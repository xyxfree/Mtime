<template>
  <div id="app">
    <ul class="headbar">
      <li>
        <a href="http://www.mtime.com/" target="_blank">首页</a>
      </li>
      <li>
        <router-link to="/" class="sc">购票</router-link>
      </li>
      <li>
        <a href="http://mall.mtime.com/"  target="_blank">正版商城</a>
      </li>
      <li>
        <a href="http://news.mtime.com/"  target="_blank">新闻</a>
      </li>
      <li>
        <a href="http://live.mtime.com/"  target="_blank">直播</a>
      </li>
      <li>
        <a href="http://movie.mtime.com/"  target="_blank">发现</a>
      </li>
      <li>
        <a href="http://www.mtime.com/community/"  target="_blank">社区</a>
      </li>
      <li>
        <a href="http://vip.mtime.com/"  target="_blank">会员</a>
      </li>
      <li class="center">
        <a href="http://www.mtime.com/" title="Mtime"  target="_blank">Mtime时光网</a>
      </li>
       <li class="register">
        <router-link to="/register">注册</router-link>
      </li>
      <li class="login" @click="watch">
        <a href="javascript:">登录</a>
        <i class="sanjiao" v-show="see"></i>
         <div class="headtip" v-show="see">
              <dl class="logintool">
                <dt>
                  <strong>为爱电影的人</strong>
                  For people who love movies
                </dt>
                <dd class="userlogin">
                    <div class="erd">
                      <div class="email">
                         <span class="namer">用户名</span>
                         <input type="text" placeholder="输入电子邮箱/手机号" class="tip">
                      </div>
                      <div class="pass">
                         <span class="password">输入密码</span>
                         <input type="password" placeholder="输入密码" class="tip">
                      </div>
                    </div>
                    <p class="usertip">
                      <a class="forget" target="_blank" href="https://passport.mtime.com/findpwd/phone">忘记密码</a>
                      <i class="ico-check"></i>
                      记住我
                    </p>
                    <div class="loginbtn">
                      <input type="button" value="登录" class="enter">
                      <router-link class="taketo" to="/register">成为会员</router-link>
                    </div>
                    <div class="otherlogin">
                      <div class="other">使用第三方登录</div>
                      <div class="round">
                        <a class="sina"
                        href="https://api.weibo.com/oauth2/authorize?client_id=166678827&response_type=code&redirect_uri=https%3a%2f%2fpassport.mtime.com%2funitelogin%2fnotify%2fweibo%2f&state=24L0rp0U_SPmxJEvZg7FrThVl1YnnwluLGO_AxIKIEYqmt543wcuFM4y81T94axddby6urlmwDtUg7NV9jCoFdQ_SAm_Ss1aP6lTCwDGRpq91LI"
                        ></a>
                        <a class="qq"
                        href="https://graph.qq.com/oauth2.0/show?which=Login&display=pc&response_type=code&client_id=101138472&redirect_uri=https%3a%2f%2fpassport.mtime.com%2funitelogin%2fnotify%2fqq%2f&state=_S2nCgRer0tvVQmvnYmBUQG8Uk_SPsba5_SrMWGxudq_A7XOVgeNWg7Hw_A1X_AhlH9aCZWBj0V0f7cmvo7UuWJyad7mrFzDUFjQmJLpVQxXxzFMw"
                        ></a>
                      </div>
                    </div>
                </dd>
              </dl>
         </div>
      </li>
      <li class="app">
        <a href="">App下载</a>
        <img class="mage" src="//img5.mtime.cn/mg/2018/01/22/200851.63552497.jpg" alt="扫描二维码下载APP">
      </li>
    </ul>
    <router-view/>
    <foot></foot>
  </div>
</template>

<script>
import foot from "./components/foot/foot";
export default {
  name: 'app',
  components: {
    foot
  },
  data() {
    return{
      see:false
    }
  },
  methods: {
    watch(){
      this.see = ! this.see
    }
  }
}
</script>

<style>
dl,dt,dd,p{
  margin: 0;
  padding: 0;
}
a{
  text-decoration: none;
}
body{
  margin: 0;
}
ul{
  padding: 0;
  margin: 0;
  list-style: none;
}
.headbar ul{
   height: 30px;
}
li{
  float: left;
  margin-right: 10px;
}
.headbar li  a{
  text-decoration: none;
  color:#c8c8c8;
  display: inline-block;
  line-height: 60px;
  margin-right: 23px;
  position: relative;
}
.headbar li a:hover{
  color:white;
}
.headbar{
  background: #192332;
  width: 100%;
  height: 60px;
  padding-left: 20px;
  position: fixed;
  z-index: 5;
  font-size: 14px;
}
.headbar .center{
  width: 117px;
  height: 36px;
  position: absolute;
  left: 50%;
  top: 50%;
  margin-left: -58px;
  margin-top: -18px;
  font-size: 100%;
}
.center a{
  background: url(//static1.mtime.cn/20170731144154/images/2014/head.png) no-repeat 0 -315px;
  width: 117px;
  height: 36px;
  display: block;
  font-size: 0;
  line-height: 0;
}
.register{
  float: right;
  margin-right: 100px;
  padding-left: 23px;
  border-left: 1px solid #303947;
}
.app{
  float: right;
  padding-left: 23px;
  position: relative;
}
.mage{
  width: 355px;
  height: 222px;
  position: absolute;
  top:62px;
  right: -30px;
  display: none;
}
.app:hover .mage{
  display: block;
}
.login{
  float: right;
  padding-left: 23px;
  border-left: 1px solid #303947;
  position: relative;
}
.login .sanjiao{
  width: 0;
  height: 0;
  overflow: hidden;
  border-bottom: 5px solid #fff;
  border-left: 7px solid transparent;
  border-right: 7px solid transparent;
  position: absolute;
  left: 50%;
  bottom: 0;
  margin-left: -7px;
}
.headtip{
  width: 245px;
  padding: 20px;
  right: -100px;
  background: #fff;
  box-shadow: 0 3px 5px rgba(0,0,0,.25);
  position: absolute;
  top: 60px;
  border: 1px solid #f5f5f5;
  border-top: 0;
}
.logintool dt{
  text-align: center;
  font-size: 16px;
  color: #9b9b9b;
  background: url(//static1.mtime.cn/20170731144154/images/2014/topbar.png) 0 -205px;
  height: 48px;
  width: 242px;
  overflow: hidden;
  line-height: 400px;
}
.logintool dt strong{
  display: block;
  font-size: 0;
  font-weight: lighter;
  color: #333;
  padding-bottom: 3px;
  line-height: 0;
}
.email,.pass{
  border: 1px solid #9b9b9b;
  margin: 10px 0 0;
  border-radius: 5px;
  position: relative;
}
.email .namer,.pass .password{
  background: url(//static1.mtime.cn/20170731144154/images/2014/head.png) no-repeat #f9f9f9;
  width: 55px;
  height: 36px;
  border-right: 1px solid #d7d7d7;
  line-height: 0;
  font-size: 0;
  border-radius: 5px 0 0 5px;
  background-position: 0 -75px;
  display: inline-block;
  position: relative;
  zoom: 1;
  vertical-align: middle;
}
.email .tip,.pass .tip{
  border: 0;
  outline: none;
  width: 165px;
  padding: 0 5px;
  background: 0;
  color: #949494;
}
.pass .password{
  background-position: -58px -75px;
}
.usertip {
  margin: 10px 0 15px 0;
  line-height: 24px;
  color: #333;
}
.userlogin .erd{
  height: 96px;
}
.headbar li .forget{
float: right;
color:black;
display: inline-block;
line-height: 0px;
margin-top: 10px;
}
.headbar li .forget:hover{
  color:plum;
}
.usertip i{
  margin-right: 5px;
  width: 27px;
  height: 27px;
  background-position: -28px -120px;
  vertical-align: top;
  cursor: pointer;
  display: inline-block;
  background: url(//static1.mtime.cn/20170731144154/images/2014/head.png) 0 -120px no-repeat;
  position: relative;
  top: -2px;
}
.enter{
  width: 112px;
  height: 30px;
  line-height: 30px;
  color: #fff;
  border-radius: 50px;
  text-align: center;
  font-size: 15px;
  position: relative;
  background: #1e7dd7;
  border: none;
  outline: none;
  cursor: pointer;
}
.headbar li .taketo{
  width: 110px;
  height: 28px;
  line-height: 28px;
  margin-left: 10px;
  background: #f4f4f4;
  color: #333;
  border: 1px solid #d9d9d9;
  border-radius: 50px;
  text-align: center;
  font-size: 15px;
  display: inline-block;
  position: relative;
  vertical-align: middle;
  margin-right: 0;
}
.headbar li .taketo:hover{
  background: #1e7dd7;
}
.otherlogin{
  background: #f5f5f5;
  padding: 20px;
  border-top: 1px solid #ddd;
  margin: 20px -20px -20px;
  border-radius: 0 0 5px 5px;
}
.otherlogin .other{
  text-align: center;
  font-weight: 700;
  font-size: 16px;
  line-height: 1;
  color: #999;
}
.otherlogin .round{
  text-align: center;
  padding: 20px 0 0;
}
.headbar li .sina,.headbar li .qq{
  background: url(//static1.mtime.cn/20170731144154/images/2014/head.png) no-repeat;
  background-position: 0 -150px;
  width: 42px;
  height: 42px;
  margin: 0 13px;
  display: inline-block;
  position: relative;
  zoom: 1;
  vertical-align: middle;
}
.headbar li .qq{
  background-position: -44px -150px;
}
</style>
