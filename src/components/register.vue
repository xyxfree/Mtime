<template>
  <div class="back">
    <div class="regin">
      <div class="regin_line"></div>
        <div class="regin_inner clearfix">
            <div class="regin_left">
             <h5>新会员注册</h5>
              <dl>
                <dd>
                  <div class="reg_tet">
                    <input type="text" placeholder="常用手机号">
                  </div>
                </dd>
                <dd>
                  <div class="reg_tet">
                    <input type="text" placeholder="密码(6-20位字母与数字.符号组合)">
                    <div class="passdbox">
                      <p class="passwordstrong">密码强度</p>
                      <p class="">
                        <i class="ps1">&nbsp;</i>
                         <i>&nbsp;</i>
                          <i>&nbsp;</i>
                      </p>
                    </div>
                  </div>
                </dd>
                <dd>
                  <div class="vcode">
                    <input type="text" placeholder="点击获取验证码">
                  </div>
                </dd>
                <dd>
                  <div class="reg_tet">
                    <input type="text" placeholder="短信验证码">
                    <a class="telcode" href="">获取验证码</a>
                  </div>
                </dd>
                <dd class="reg_btn">
                    <a href="" class="btn_blue">注册</a>
                </dd>
              </dl>
            </div>
            <div class="regin_right">
              <h5>会员登录</h5>
              <dd>
                <div class="reg_tet">
                  <input type="text" placeholder="登录邮箱/手机号码">
                </div>
              </dd>
              <dd>
                <div class="reg_tet">
                  <input type="text" placeholder="请输入密码">
                </div>
              </dd>
              <dd>
                <div class="bind">
                  <a href="https://passport.mtime.com/findpwd/phone?token=eyJtb2JpbGUiOiIifQ==">忘记密码</a>
                </div>
              </dd>
              <dd>
                <div class="isautosign">
                  <a href="">登录</a>
                </div>
              </dd>
              <div class="regbtn">
                <a href=""></a>
              </div>
              <div class="otherlogins">
                <div class="others">使用第三方登录</div>
                  <div class="rounds">
                    <a class="sinas"
                    href="https://api.weibo.com/oauth2/authorize?client_id=166678827&response_type=code&redirect_uri=https%3a%2f%2fpassport.mtime.com%2funitelogin%2fnotify%2fweibo%2f&state=24L0rp0U_SPmxJEvZg7FrThVl1YnnwluLGO_AxIKIEYqmt543wcuFM4y81T94axddby6urlmwDtUg7NV9jCoFdQ_SAm_Ss1aP6lTCwDGRpq91LI"
                    ></a>
                    <a class="qqs"
                      href="https://graph.qq.com/oauth2.0/show?which=Login&display=pc&response_type=code&client_id=101138472&redirect_uri=https%3a%2f%2fpassport.mtime.com%2funitelogin%2fnotify%2fqq%2f&state=_S2nCgRer0tvVQmvnYmBUQG8Uk_SPsba5_SrMWGxudq_A7XOVgeNWg7Hw_A1X_AhlH9aCZWBj0V0f7cmvo7UuWJyad7mrFzDUFjQmJLpVQxXxzFMw"
                      ></a>
                  </div>
              </div>
            </div>
      </div>
    </div>
  </div>
</template>
<style>
.back{
  padding:60px 0 60px;
  background-color: rgb(238, 233, 233);
}
.back .regin{
  background: #fff;
  width: 1000px;
  margin: 90px auto 0px;
  border-radius: 6px;
  position: relative;
  padding-bottom: 30px;
  min-height: 500px;
}
.regin_line{
  background: linear-gradient(#fff,#dedede 10%,#dedede 90%,#fff);
  width: 1px;
  height: 482px;
  overflow: hidden;
  position: absolute;
  left: 50%;
  top: 50px;
}
.regin_inner{
  padding: 30px 65px;
}
.regin_left{
  float: left;
  width: 380px;
}
.regin_inner  .regin_left h5{
  font-size: 30px;
  line-height: 1em;
  text-align: center;
  padding-bottom: 10px;
  font-weight: 400;
  margin: 0;
}
.reg_tet{
  position: relative;
  border: 1px solid #aaa;
  zoom: 1;
  height: 49px;
  width: 373px;
  margin-top: 23px;
  border-radius: 4px;
  vertical-align: baseline;
  display: inline-block;
  z-index: 1;
}
.reg_tet input{
  background: none;
  height: 21px;
  border: none;
  padding: 14px;
  line-height: 21px;
  font-size: 14px;
  width: 345px;
}
.reg_tet .passdbox{
  color: #949494;
  position: absolute;
  right: 10px;
  top: 11px;
  font-size: 12px;
}
.passdbox p:last-child {
  line-height: 0;
  font-size: 0;
}
.passdbox i{
  background: #c5c5c5;
  overflow: hidden;
  display: inline-block;
  width: 14px;
  height: 4px;
  margin-right: 3px;
  margin-top: 5px;
  font-weight: 400;
}
.vcode{
  width: 210px;
  position: relative;
  zoom: 1;
  margin-top: 23px;
  border-radius: 4px;
  vertical-align: baseline;
  display: inline-block;
  z-index: 1;
  border: 1px solid #aaa;
}
.vcode input{
  width: 182px;
  background: none;
  height: 21px;
  border: none;
  padding: 14px;
  line-height: 21px;
  font-size: 14px;
}
.telcode{
  background: #f6f6f6;
  height: 34px;
  border: 1px solid #b6b6b6;
  position: absolute;
  right: 10px;
  top: 7px;
  font-size: 14p;
  line-height: 34px;
  padding: 0 15px;
  color: #333;
  border-radius: 3px;
}
.reg_btn{
  text-align: center;
  padding-top: 35px;
}
.reg_btn .btn_blue{
  background: #0081bc;
  width: 257px;
  height: 53px;
  display: inline-block;
  position: relative;
  font-size: 20px;
  line-height: 53px;
  border-radius: 27px;
  color: #fff;
  text-align: center;
  vertical-align: middle;
}
.regin_right{
  float: right;
  width: 380px;
}
.regin_right h5 {
  font-size: 30px;
  line-height: 1em;
  text-align: center;
  padding-bottom: 10px;
  font-weight: 400;
  margin: 0;
}
.bind{
  padding-top: 20px;
  font-size: 14px;
  text-align: right;
}
.isautosign{
  text-align: center;
  padding-top: 35px;
}
.isautosign a{
  background: #0081bc;
  width: 257px;
  height: 53px;
  display: inline-block;
  position: relative;
  zoom: 1;
  overflow: hidden;
  font-size: 20px;
  line-height: 53px;
  border-radius: 27px;
  color: #fff;
  text-align: center;
  vertical-align: middle;
}
.otherlogins{
  padding: 20px;
  margin: 20px -20px -20px;
  border-radius: 0 0 5px 5px;
}
.otherlogins .others{
  text-align: center;
  font-weight: 700;
  font-size: 16px;
  line-height: 1;
  color: #999;
}
.otherlogins .rounds{
  text-align: center;
  padding: 20px 0 0;
}
.otherlogins .sinas,.otherlogins .qqs{
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
.otherlogins .qqs{
  background-position: -44px -150px;
}
</style>
