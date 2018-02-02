<template>
  <div class="filmtip">
    <div class="filmtipbox">
      <ul class="clearfix">
        <li class="first">
          <a href="http://piao.mtime.com/" target="_blank">
            <div class="moviecard">
              <div class="cardbg"></div>
              <div class="cardbg1"></div>
              <dl>
                <dt>时光电影卡</dt>
                <dd>尊享3-6折优惠,支持在线选座</dd>
                <dd>企业个性化定制</dd>
                <dd>商务馈赠，节日送礼，员工福利</dd>
              </dl>
            </div>
          </a>
        </li>
        <li class="centered">
          <div class="ticketonline">
            <h2>如何在线钻做购票</h2>
            <p></p>
          </div>
        </li>
        <li class="last">
          <span>
            <b>客服电话 : </b>
            4006-118-118
          </span>
          <b class="sty">影院商务合作 : </b>
          <a href="http://theater.mtime.com/report/1" target="_blank">影院开业</a>
          <span class="mline">|</span>
          <a href="http://theater.mtime.com/report/4/" target="_blank">影讯合作</a>
          <span class="mline">|</span>
          <a href="http://theater.mtime.com/report/2/" target="_blank">在线购票</a>
          <span class="mline">|</span>
          <a href="http://theater.mtime.com/report/1/" class="our" target="_blank">联系时光网</a>
        </li>
      </ul>
    </div>
  </div>
</template>
<style>
p{
  margin: 0;
}
ul{
  padding: 0;
  margin: 0;
  list-style: none;
}
.filmtip{
  background: #0081bc;
  padding: 30px 0;
  position: relative;
  zoom: 1;
}
.filmtipbox{
  width: 1000px;
  margin: auto;
  overflow: hidden;
}

.filmtipbox li {
  background: #e1eef4;
  padding: 15px 20px;
  width: 490px;
  border-radius: 5px;
  float: left;
  display: inline;
  margin: 0 0 10px 10px;
}
 .filmtipbox  .first{
  width: 420px;
  margin-left: 0;
}
.first  a{
   cursor: pointer;
}
.moviecard{
  height: 140px;
  position: relative;
  zoom: 1;
  padding-left: 180px;
}
.moviecard .cardbg{
  background: url(//static1.mtime.cn/theater/20170719092733/images/filmmovie.jpg) no-repeat 0 -104px;
  width: 182px;
  height: 146px;
  left: -20px;
  top: -20px;
  position: absolute;
}
.moviecard .cardbg1{
  background: url(//static1.mtime.cn/theater/20170719092733/images/cinema_png.png) no-repeat 0 -228px;
  width: 110px;
  height: 90px;
  bottom: -20px;
  left: -20px;
  position: absolute;
}
.moviecard dt{
  color: #033333;
  font-size: 18px;
  line-height: 26px;
  font-weight: bold;
  padding-bottom: 10px;
}
.moviecard dd{
  font-size: 14px;
  line-height: 26px;
  padding: 0;
}
.ticketonline h2{
  font-size: 18px;
  line-height: 26px;
  color: #033333;
}
.ticketonline p{
  width: 450px;
  height: 104px;
  margin: 10px auto 0;
  background: url(//static1.mtime.cn/theater/20170719092733/images/filmmovie.jpg) no-repeat;
}
.filmtipbox  .last{
  width: 960px;
  margin: 0;
}
 .last span:nth-of-type(1){
  font-size: 20px;
  float: right;
  line-height: 28px;
 }
.last span b{
  font-weight: bold;
  font-size: 18px;
  color: #033333;
  font-style: normal;
}
.sty{
  font-weight: bold;
  font-size: 18px;
  color: #033333;
}
.last a{
  font-size: 14px;
  line-height: 28px;
}
.mline{
  padding: 0 10px;
  color: #333;
}
.our{
  display: inline-block;
  font-size: 14px;
  line-height: 28px;
  border-radius: 14px;
  width: 110px;
  height: 28px;
  background-color: rgb(32, 167, 32);
  text-align: center;
  color: #fff;
}
.our:hover{
  background-color: red;
}
</style>
