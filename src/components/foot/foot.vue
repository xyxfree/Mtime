<template>
  <footer class="footer">
			<div class="word clearfix">
				<div class="fotdogo">
					<dl>
						<dt>
							<a href="http://www.mtime.com/">
                <img :src="time" width="122" alt="">
              </a>
						</dt>
						<dd class="clearfix">
							<a href="http://jobs.mtime.com/">加入我们</a>
							<a href="http://feature.mtime.com/help/contact.htm">联系我们</a>
						</dd>
						<dd class="clearfix">
							<a href="http://group.mtime.com/help/">站务论坛</a>
              <router-link to="/register">问题反馈</router-link>
						</dd>
						<dd class="clearfix">
							<a href="http://feature.mtime.com/help/rules.htm">社区准则</a>
							<a href="http://www.mtime.com/sitemap.htm">网站地图</a>
						</dd>
						<dd class="clearfix">
							<a href="http://feature.mtime.com/help/privacy.htm">隐私政策</a>
							<a href="http://en.mtime.com/">English</a>
						</dd>
					</dl>
				</div>
				<div class="fotmap">
					<dl class="fotmap-left">
						<dt>栏目</dt>
						<dd>
              <a href="http://news.mtime.com/">新闻</a>
            </dd>
						<dd>
              <a href="">影院</a>
            </dd>
						<dd>
              <a href="http://mall.mtime.com/">商城</a>
            </dd>
						<dd>
              <a href="http://www.mtime.com/community/">社区</a>
            </dd>
					</dl>
					<dl class="fotmap-right">
						<dt>推荐</dt>
						<dd>
							<a href="http://movie.mtime.com/recent/">观影指南</a>
							<a href="http://movie.mtime.com/boxoffice/">电影票房</a>
						</dd>
						<dd>
							<a href="http://news.mtime.com/conversation/">时光对话</a>
							<a href="http://video.mtime.com/trailer/">新片预告</a>
						</dd>
						<dd>
							<a href="http://movie.mtime.com/all/list/index.html">特色榜单</a>
              <router-link to="/register">电影猜猜猜</router-link>
						</dd>
						<dd>
							<a href="http://news.mtime.com/fun/">全球拾趣</a>
               <router-link to="/register">卡片大富翁</router-link>
						</dd>
					</dl>
				</div>
				<div class="fotweek">
					<dl class="clearfix">
						<dt>
							<strong>时光周刊</strong>
							<span>第207期</span>
						</dt>
						<dd>
              <a href="http://www.mtime.com/weekly/" target="_blank">
                <img :src="map" alt="">
              </a>
						</dd>
					</dl>
				</div>
				<div class="fothr">
					<dl>
						<dt>
							<strong>手机购票</strong>
							方便实惠
						</dt>
						<dd>
							<img :src="code" alt="">
						</dd>
						<dd>扫描二维码 下载客户端</dd>
					</dl>
				</div>
			</div>
			<div class="foot">
				<p>
					<span>北京动艺时光网络科技有限公司</span>
					Copyright 2006-2018 Mtime.com Inc. All rights reserved.
					<br>
					<br>
					<a target="_blank" href="http://feature.mtime.com/help/icp.htm">京ICP证050715号</a>
				  <a target="_blank" href="http://feature.mtime.com/help/videolicence.htm"> 网络视听许可证0108265号</a>
					<a target="_blank" href="http://feature.mtime.com/help/network.htm"> 网络文化经营许可证</a>
					<a target="_blank" href="http://feature.mtime.com/help/tvlicence.htm"> 广播电视节目制作经营许可证(京)字第1435号</a>
          <a>京公网安备：110105000744号</a>
				</p>
				<div class="credible">
					<a href="http://feature.mtime.com/help/credible.htm" target="_blank">
            <img :src="trademark" alt="">
          </a>
					<a href="http://feature.mtime.com/help/goodfaith.htm" target="_blank">
            <img :src="Sincerity" alt="">
          </a>
				</div>
			</div>
		</footer>
</template>
<script>
import map from './map.jpg'
import code from './code.png'
import time from './time.png'
import trademark from './trademark.jpg'
import Sincerity from './Sincerity.jpg'
export default {
  data() {
    return {
      map,
      code,
      time,
      trademark,
      Sincerity
    }
  }
}

</script>
<style>
.footer{
	border-top:2px solid red;
  background: #f7f7f7;
}
.word{
  width: 1000px;
  height: 202px;
  margin: 0 auto;
  padding-top: 40px;
  font-size: 13px;
}
.fotdogo{
	width: 200px;
  float: left;
  position: relative;
  min-height: 157px;
	border-right: 1px solid plum;
}
.fotdogo dl{
	padding-bottom: 10px;
	padding: 0 20px;
}
.fotdogo dd{
	font-size: 13px;
	color: #323232;
	line-height: 1.8em;
}
.fotdogo dd a:nth-of-type(2){
	margin-left: 40px;
}
.fotmap{
	width: 325px;
  float: left;
  display: inline;
  position: relative;
  min-height: 157px;
	font-size: 13px;
	border-right: 1px solid plum;
}
.fotmap .fotmap-left{
	width: 42px;
  float: left;
  display: inline;
  margin-left: 33px;
  line-height: 2em;
}
.fotmap .fotmap-left dd,.fotmap .fotmap-right dd{
	font: 16px/32px '微软雅黑';
}
.fotmap-right dd a:nth-of-type(2){
	margin-left: 35px;
}
.fotmap-right{
	width: 185px;
  float: left;
  display: inline;
  margin-left: 33px;
  line-height: 2em;
}
.fotweek{
	width: 230px;
  float: left;
  display: inline;
  min-height: 157px;
	font-size: 13px;
	border-right: 1px solid plum;
}
.fotweek dl{
	width: 172px;
  margin: 0 auto;
}
.fotweek strong{
	font-size: 18px;
  font-weight: normal;
}
.fotweek span{
	float: right;
	color: #7d7d7d;
  padding-top: 3px;
}
.fotweek dd{
	margin-top: 25px;
}
.fothr{
	width: 155px;
  float: left;
  display: inline;
  min-height: 157px;
  text-align: center;
	font-size: 13px;
}
.fothr dd{
	margin-top: 12px;
}
.foot{
	background: #f7f7f7;
  color: #7e7e7f;
  text-align: center;
  font-family: verdana,"宋体";
  padding: 30px 0 20px;
	font-size:14px;
}
.foot span{
	margin-right: 12px;
	color: #7e7e7f;
}
.foot a{
	margin-right: 12px;
	text-decoration: none;
  font:15px/15px "宋体" ;
  cursor: pointer;
	vertical-align: baseline;
	color: #333;
}
.footer a{
  color: #333;
}
.footer a:hover{
  color: #08c;
}
.credible{
  text-align: center;
  padding-top: 12px;
}
.credible img{
	margin-right: 10px;
}
</style>
