# 全分片主链(Layer-1)

## 概述

Layer-1扩展指的是区块链本身的直接性能改进。在所有的链上扩容方案中，分片技术得到了最多的关注，并且通常被认为是无许可公链的最佳路径。然而，到目前为止，大多数的分片尝试都只是在计算方面分片，不涉及状态和网络容量。 

TOP Network在计算、状态和网络这三个方面，成为了一个全面、多层动态分片的典范。这主要得益于Layer-0的底层网络基础设施、分层的共识网络、VRF的排序算法、双层点阵-DAG数据结构和并行的pBFT-PoS*共识机制。这些创新使TOP Network实现线性扩容成为可能，同时还保证了无许可状态下TOP Network的安全性和完整性。

## 主链架构

![Snap114](ComprehensiveMulti-levelDynamicSharding(layer-1).assets/Snap114.jpg)



## Sub-Beacon网络

TOP Network Sub-Beacon主要负责auditor、validator选举及工作量统计、审计、惩罚等工作。

## 三层共识网络

TOP Network的共识网络分为三层：

The Edge Network：充当客户端的接入点，所有交易在被转发到路由网络之前都会被先发送给边缘网络的边缘节点。

The Audit Network：由随机划分为分片的审计节点组成。此层网络负责处理跨分片通信和同步，同时参与交易验证。当前Audit Network有2个分片，每个分片下辖2个Validate Network分片。

The Validate Network：由包含验证节点的分片组成。这里是进行交易验证的地方。在每个分片中，验证节点使用并行pBFT算法验证和确认交易。

TOP Network出于多种原因而使用分层网络。首先，多种类型节点之间划分职责有助于降低对节点的要求。路由网络处理大多数对带宽要求较高的需求，例如跨分片通信，这就允许降低对验证节点的带宽要求。此外，因为客户端只能将交易直接发送到边缘节点，从而保护路由和核心网络免受泛滥交易的攻击。

TOP Network所有网络都支持分片扩展。

## VRF-FTS 随机分片算法

安全性是分片技术面临的最大挑战之一。将网络拆分成一个个小组后，恶意节点攻占分片变得更加容易，我们称这种攻击为“单片接管攻击(Single-Shard Takeover Attack)”。为了防止这种情况，分片都是随机进行的。随机分片让攻击变得越来越难，因为恶意实体无法让它们的节点进入任何特定的分片，降低合谋概率。

为了在分布式系统里做到随机性，TOP Network使用了可验证随机函数(Verifiable Random Function)。VRF是一种将输入映射为可验证的伪随机输出的加密方案，允许创建无法被预测，却可被公开验证的随机种子。这些通过VRF生成的随机种子，经过"FTS(follow-the-satoshi)"算法加权计算后生成随机数，将验证节点随机加入到分片中，以及将审计节点随机加入到集群中。

## 动态分片

虽然随机分片有助于防止攻击者直接将其节点插入到特定分片，但是它不足以抵抗通过逐渐渗透、破坏分片的自适应攻击。例如，如果有足够的时间，恶意实体可能会“贿赂”特定分片中的所有节点。如果分片的节点组成保持不变，则这种贿赂攻击是可行的。为了防止这种情况，TOP Network采用动态分片。每隔一段时间，分片中的一些节点会被重新分配到节点候选池，当其他分片进行选举时，这些节点会从候选池被选举到新分片。随着时间的推移，分片将具有与先前完全不同的节点。因为每次仅有少数节点被重新分配，当节点分配到新分片的时候，会同步新分片的区块数据，所以分片的共识过程不会被中断。

在路由/审核网络中也是采取同样的方法，其中审计节点是持续在集群之间被重新分配。此双层动态分片方案让自适应攻击变得几乎不可能。 

## 多级分片

分片的目的是实现系统性能的线性扩展。这意味着可扩展性随节点数量的增加而线性增加。为了实现线性扩展，单个节点工作量必须脱离节点总数和全网交易总量。

为此，必须对区块链的所有资源进行分片处理，包括状态（存储）、计算（交易验证和智能合约执行）和网络（区块广播、跨分片通信等）。如果仅对计算分片，则存储或带宽将最终成为系统瓶颈。为了达到全分片系统的目标，我们开发了一种新颖的多层分片架构。即每种区块链资源都以多种方式分片，这种分片方法有助于提高系统可扩展性和降低对节点的要求。 

## 双层状态分片

TOP Network链的状态信息包括所有用户账户和智能合约的状态信息。每个用户账户和智能合约都由一个账户数据对象表示。每个账户对象包含多个属性、关联函数和一个小型NoSQL数据库。

状态以两种方式分片。

首先，分片里的账户都是独立的，节点物理机只存储节点所在分片里的账户状态信息，虽然这已经实现了全局状态的分区，但是由于一些原因，这还不够。由于验证节点只存储与该分片关联的子账户空间的状态信息，因此它们无法充分验证从其他分片发送的交易，除非它们知道发送交易的账户状态已正确更新。

考虑到这点，我们使用表，这些表存储最近有过变更的账户的最新状态信息。当前所有的分片平分1024个表。账户需要被均匀平分，以便每个表负责大小相等的账户子空间。通过账户交易的Hash值可以快速确定账户与表的关系。这使得分片可以快速地从其他分片中提取相关状态信息，并在提交交易之前检查是否正确地更新了余额。

表还可用于批处理交易从而提高吞吐量。来自同一账户，及同一子账户空间中其他账户的多比交易，可以一起被打包在一个表中。这些表可以在一轮共识中被同时验证，大大提高了系统吞吐量。 

## 三层计算分片

交易验证和智能合约的执行都需要消耗计算资源，两者都是hpPBFT共识机制。我们使用三层设计来实现可靠的计算分片。当交易被分发到分片进行验证时，该分片中的部分节点被随机选中用于hpPBFT共识验证。

分片的其余节点可以监视验证节点并辅助随后的同步过程。集群中的审计节点也通过二次审计参与hpPBFT共识验证。

