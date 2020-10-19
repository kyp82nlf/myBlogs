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
    font-size:22px;
    font-family:SourceSansPro-Bold;
    font-weight:bold;
    color:rgba(0,0,0,1);
    padding-bottom: 10px;
    border-bottom: 1px solid #979797;
    text-align:left;
    margin-bottom:10px;
  }
  .content-container {
    margin:40px 120px;
    padding:40px 30px;
    background:rgba(245,247,247,1);
  }
  .content-container .content-row:first-child {
    margin-bottom: 40px;
  }
  @media screen and (max-width:576px) {
     .content-container {
        margin:40px 20px;
    }
  }
  </style>
  <body>
  <h1 align="center">Top开发者中心</h1>
  <div >欢迎来到Top开发者中心。借助完善的开发者文档，你可以快速了解Top的生态、技术和工具。</div>
    <div ></br></br>
    <!--
      <h4>关于Top</h4>
      <div class="content-container" style="background-color: #f4f4f4;padding: 1.2rem 1.2rem 2.4rem;margin: 2.4rem 0;" >
          <div class="row content-row">
            <div class="col-sm-4 col-xs-12">
                <p class="content-title" style="border-bottom: 1px solid #979797;">认识Top</p>
                  <div>
                      <div>
                          <a href="javascript:void(0)">介绍</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">Top 共识</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">智能合约</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">查看全部</a>
                      </div>
                  </div></br>
            </div>
            <div class="col-sm-4 col-xs-12">
                <p class="content-title" style="border-bottom: 1px solid #979797;">Top客户端</p>
                  <div>
                      <div>
                          <a href="javascript:void(0)">概述</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">快速开始</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">连接到TOP</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">Restful 接口</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">查看全部</a>
                      </div>
                  </div>
            </div>
      </div>
      -->
      <h4>工具</h4>
      <div class="content-container" style="background-color: #f4f4f4;padding: 1.2rem 1.2rem 2.4rem;margin: 2.4rem 0;">
          <div class="row content-row">
          <!--
            <div class="col-sm-4 col-xs-12">
                <p class="content-title"  style="border-bottom: 1px solid #979797;">智能合约 </p>
                  <div>
                      <div>
                          <a href="javascript:void(0)">概述</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">快速开始</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">Restful 接口</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">查看全部</a>
                      </div>
                  </div>
            </div>
            -->
            <div class="col-sm-4 col-xs-12">
                <p class="content-title"  style="border-bottom: 1px solid #979797;">SDKs</p>
                  <div>
                      <div>
                          <a href="#/docs-en/SDKs/00-overview">Overview</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="#/docs-en/SDKs/02-c++-sdk">C++ SDK</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="#/docs-en/SDKs/01-javascript-sdk">JavaScript SDK</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="#/docs-en/SDKs/03-java-sdk">Java SDK</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="#/docs-en/SDKs/00-overview">View all</a>
                      </div>
                  </div>
            </div>
            <!--
            <div class="col-sm-4 col-xs-12">
                <p class="content-title"  style="border-bottom: 1px solid #979797;">区块链浏览器 API</p>
                  <div>
                      <div>
                          <a href="javascript:void(0)">概述</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">快速开始</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">Restful 接口</a>
                      </div>
                  </div>
                  <div>
                      <div>
                          <a href="javascript:void(0)">查看全部</a>
                      </div>
                  </div>
            </div>
            -->
          </div>
      </div>
    </div>
  </body>
</html>
