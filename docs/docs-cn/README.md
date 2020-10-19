
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <title>docs_homepage</title>
<link href="https://cdn.bootcss.com/twitter-bootstrap/4.2.1/css/bootstrap.min.css" rel="stylesheet">

</head>

  <style scoped >
  h1, h2 {
    font-weight: normal;
  }
  ul {
    /* list-style-type: none; */
    padding: 0;
    text-align: left;
  }
  li {
    display: block;
    margin: 0;
  }
  ul a {
      font-size:22px;
  font-family:SourceSansPro-Regular;
  font-weight:400;
  color:rgba(110,111,112,1);
  position: relative;
  padding-left: 10px;
  }
  li a::before {
    content: '';
    width:4px;
    height:4px;
    border-radius: 50%;
    background:#000000;
    position: absolute;
      /* display: block; */
      left: 0;
      top: 15px;
  }
  .content-title {
    font-size:18px;
    font-family:SourceSansPro-Bold;
    font-weight:bold;
    color:#444;
    padding-bottom: 10px;
    border-bottom: 1px solid #979797;
    text-align:left;
    margin-bottom:10px;
  }
  .content-container .content-row {
  	display: -webkit-box;
		display: -moz-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-pack: justify;
		-moz-box-pack: justify;
		-ms-flex-pack: justify;
		justify-content: space-between;
  }
  .markdown-section h4 {
  	font-size: 1.5em;
  }
  .content-row-item {
  	width: 48%;
  	padding: 20px;
  	margin-bottom: 30px;
  }
  .content-row-item:nth-child(2n+1) {
  	background: linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%);
  	background: -webkit-linear-gradient(t157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* Safari 5.1-6.0 */
    background: -o-linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* Opera 11.1-12.0 */ 
    background: -moz-linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* Firefox 3.6-15 */
    background: linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* 标准语法 */
  }
  .content-row-item:nth-child(2n+2) {
  	background: linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%);
  	background: -webkit-linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* Safari 5.1-6.0 */
    background: -o-linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* Opera 11.1-12.0 */ 
    background: -moz-linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* Firefox 3.6-15 */
    background: linear-gradient(157deg, rgba(252, 237, 219, 0.2) 0%, rgba(191, 143, 93, 0.2) 100%); /* 标准语法 */
  }
  .markdown-section a {
  	color: #666;
  }
  .close:not(:disabled):not(.disabled):focus, .close:not(:disabled):not(.disabled):hover {
    opacity: 1;
	}
	.close:not(:disabled):not(.disabled) {
    cursor: inherit;
	}
	.close {
    float: inherit;
    font-size: inherit;
    font-weight: inherit;
    line-height: 1.5;
    color: #000;
    text-shadow: inherit;
    opacity: 1;
	}
//.content-container .content-row:first-child {
//  margin-bottom: 40px;
//}
  @media screen and (max-width:576px) {
     .content-container {
    	margin:40px 0;
    }
    .content-container .content-row {
    	display: block;
    }
    .content-row-item {
	  	width: 100%;
	  	padding: 20px;
	  	margin-bottom: 30px;
	  }
  }
  </style>
  <body>
  <h1 align="center">TOP Network 开发者帮助中心</h1>
  <div >欢迎来到TOP Network开发者帮助中心。

TOP Network主链是全球首个实现完全分片的公链、完全无许可的PoS链。采用多重分片、基于DAG数据结构的双层点阵等扩容技术、以及并行hpBFT共识机制等，使单链交易处理能力达10万TPS。

强大的交易处理能力、快速的交易确认、免费的交易费用，及链安全性，适合于海量、高频业务。

借助完善的开发者文档，您可以快速了解TOP Network的生态、技术和工具，以帮助您快速与TOP Network进行互动。</div> 

<div ></br></br>
<!--
  -->
  <h4>关于 TOP Network</h4>
	<!--style="background-color: #f4f4f4;padding: 1.2rem 1.2rem 2.4rem;margin: 2.4rem 0;"-->
  <div class="content-container">
      <div class="row content-row">
        <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">认识 TOP Network</p>
              <div>
                  <div>
                      <a href="#/docs-cn/AboutTOPNetwork/TOPNetworkPlatform">TOP Network 区块链平台</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/AboutTOPNetwork/TOPChainInfrastructure/Overview">TOP Network 基础设施层</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/AboutTOPNetwork/Protocol/OverView">TOP Network 协议</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/AboutTOPNetwork/Security">链安全</a>
                  </div>
              </div>
             <div>
                  <div>
                      <a href="#/docs-cn/AboutTOPNetwork/TermList">查看全部</a>
                  </div>
              </div>
        </div>
          <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">TOP Network 节点</p>
              <div>
                  <div>
                      <a href="#/docs-cn/Node/Overview">概述</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Node/JoiningNetwork">节点入网</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Node/NodeSignature">节点签名</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Node/NodeElection">节点选举</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Node/NodeReward">节点奖励</a>
                  </div>
              </div>
             <div>
                  <div>
                      <a href="#/docs-cn/Node/NodePublishment">查看全部</a>
                  </div>
              </div>
      </div>
  </div> <div class="row content-row">
        <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">智能合约</p>
              <div>
                  <div>
                      <a href="#/docs-cn/SmartContract/SmartContract">概述</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/SmartContract/SystemContractAPI">系统智能合约 API</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/SmartContract/LuaAPI">智能合约 API</a>
                  </div>
              </div>
        </div>
          <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">链上治理</p>
              <div>
                  <div>
                      <a href="#/docs-cn/On-ChainGovernance/Overview">概述</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/On-ChainGovernance/On-ChainGovernanceProposal">链上治理流程</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/On-ChainGovernance/On-ChainGovernanceParameters">链上治理参数</a>
                  </div>
              </div>
     </div>
  </div> <div class="row content-row">
        <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">RPC API</p>
              <div>
                  <div>
                      <a href="#/docs-cn/Interface/RPC-API/Overview">概述</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Interface/RPC-API/requestToken">获取链访问身份令牌</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Interface/RPC-API/sendTransaction/sendTransaction">发送交易</a>
                  </div>
              </div>
			  <div>
                  <div>
                      <a href="#/docs-cn/Interface/RPC-API/get">查询链上信息</a>
                  </div>
              </div>
			</div>
		</div>
</div>
</div ></br></br>
<!--
  -->

  <h4>工具</h4>
  <div class="content-container">
      <div class="row content-row">
        <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">TOPIO 使用指南</p>
              <div>
                  <div>
                      <a href="#/docs-cn/Tools/TOPIO/Overview">概述</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Tools/TOPIO/InstallTOPIO">安装 TOPIO</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Tools/TOPIO/QuickStart">快速入门</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Tools/TOPIO/StartTOPIO">启动 TOPIO</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Tools/TOPIO/Command-line_Options">命令行选项</a>
                  </div>
              </div>
             <div>
                  <div>
                      <a href="#/docs-cn/Tools/TOPIO/topcl/Overview">查看全部</a>
                  </div>
              </div>
			</div>
          <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">SDKs</p>
              <div>
                  <div>
                      <a href="#/docs-cn/Interface/SDKs/00-overview">概述</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Interface/SDKs/01-javascript-sdk">JavaScript SDK</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Interface/SDKs/03-java-sdk">Java SDK</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/Interface/SDKs/02-c++-sdk">C++ SDK</a>
                  </div>
              </div>
      </div>
        </div>
       </div>

</div>
</div ></br></br>
  <h4>对接指南</h4>
  <div class="content-container">
      <div class="row content-row">
        <div class="content-row-item">
            <p class="content-title" style="border-bottom: 1px solid #979797;">钱包对接指南</p>
              <div>
                  <div>
                      <a href="#/docs-cn/AccessGuide/WalletAccessGuide/Overview">概述</a>
                  </div>
              </div>
              <div>
                  <div>
                      <a href="#/docs-cn/AccessGuide/WalletAccessGuide/SDKintegartion">SDK 集成</a>
                  </div>
              </div>
				</div>
      </div>
        </div>

</div>	  
			
  </body>
</html>

