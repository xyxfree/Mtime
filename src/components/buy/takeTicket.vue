<template>
<div>
  <div class="filmticket" :style="{height: shrink?'864px':'1360px'}">
    <div class="title clearfix">
      <h2>
        北京
        <span>{{data.film.length}}</span>
        家影院
      </h2>
    </div>
    <ul class="clearfix" v-for="item in data.film">
      <li>
        <a :href="item.mageadress" class="filmname">
          <img :src="item.mage" alt="">
        </a>
        <dl class="movieinfobox">
          <dt class="favregion">
            <a :href="item.nameaddress">{{item.name}}</a>
          </dt>
          <dd class="intotxt">
            <p>{{item.title}}</p>
            <div class="moretool">
              <span class="ico">{{item.ico1}}</span>
              <span class="ico">{{item.ico2}}</span>
              <span class="ico">{{item.ico3}}</span>
              <span class="ico">{{item.ico4}}</span>
              <span class="ico">{{item.ico5}}</span>
              <span class="ico">{{item.ico6}}</span>
            </div>
            <div class="ticketselect">
              <p>
                <span>¥</span>
                      {{item.price}}
                <span>元起</span>
              </p>
              <a :href="item.btn">选座购片</a>
            </div>
          </dd>
        </dl>
      </li>
    </ul>
  </div>
  <div class="long">
    <div class="short">
      <div class="more" @click="more">
        <i></i>
        更多
      </div>
    </div>
  </div>
  <div class="filter">
    <a href="http://feature.mtime.com/mobile/">
      <img :src="filter"  width="1000" alt="">
    </a>
  </div>
</div>
</template>
<script>
import data from '../data.js'
import filter from './filter.jpg'
  export default {
    data() {
      return{
        data,
        filter,
        shrink:true
      }
    },
    methods:{
        more(){
          this.shrink = false;
        }
    }
  }
</script>
<style scoped>
@import "./css/style.css";
/* a{
  text-decoration: none;
  color: #333;
}
.filmticket{
  width: 1000px;
  height: 864px;
  overflow: hidden;
  margin: 40px auto 0;
}
.ticketselect a:hover{
  background-color: red;
}
.title{
  border-bottom: 1px solid #a9a9a9;
}
.title h2{
  width: 200px;
  font-size: 20px;
  font-weight: normal;
  line-height: 48px;
  border-left: 10px solid #ff6d00;
  padding: 0 15px;
  float: left;
}
.favregion a:hover{
  color: #08c;
  cursor: pointer;
}
.filmticket li{
  border-bottom: 1px solid #e8e8e8;
  padding: 30px 0;
  min-height: 90px;
  position: relative;
  zoom: 1;
}
.filmname{
  width: 102px;
  height: 63px;
  border: 1px solid #a5a5a5;
  position: absolute;
  left: 0;
  top: 30px;
  z-index: 2;
}
.movieinfobox{
  border: 0;
  padding: 0 0 0 125px;
  position: relative;
  zoom: 1;
}
.favregion{
  padding-top: 0;
  margin-top: -6px;
  position: relative;
  zoom: 1;
  font-size: 24px;
  padding: 5px 0 0 0;
  min-height: 35px;
  line-height: 35px;
}
.intotxt{
  margin: 10px 0 0;
}
.intotxt p{
  font-size: 14px;
  line-height: 24px;
}
.moretool{
  text-align: left;
  margin: 10px 0 0 0;
  position: relative;
  width: 560px;
  left: 0;
}
.ico{
  width: 48px;
  height: 24px;
  border-radius: 5px;
  display: inline-block;
  text-align: center;
  line-height: 24px;
  color:#fff;
  background-color: green;
  margin-right: 5px;
}
.moretool .ico:nth-of-type(5){
  width: 108px;
}
.moretool .ico:nth-of-type(6){
  width: 78px;
}
.ticketselect{
  width: 126px;
  position: absolute;
  right: -30px;
  top: 15px;
  z-index: 2;
}
.ticketselect p{
  text-align: center;
  color: #f77603;
  font-size: 30px;
  line-height: 24px;
  height: 36px;
}
.ticketselect p span:nth-of-type(1){
  font-size: 12px;
  padding: 0 3px;
}
.ticketselect p span:nth-of-type(2){
  font-size: 12px;
  padding: 0 3px;
}
.ticketselect a{
  background: #0081bc;
  width: 94px;
  height: 25px;
  display: inline-block;
  border-radius: 15px;
  font-size: 14px;
  line-height: 25px;
  text-align: center;
  letter-spacing: 2px;
  color: #fff;
  text-decoration: none;
  position: relative;
  zoom: 1;
}
.filter,.long{
  width: 1000px;
  margin: 10px auto 10px;
}
.short{
  width: 685px;
  height: 82px;
  position: relative;
}
.more{
  color: #333;
  position: absolute;
  bottom:30px;
  left: calc(50% - 36px);
  cursor: pointer;
}
.more i{
  background: url(//static1.mtime.cn/theater/20170719092733/images/allicon24.png) no-repeat -267px -336px;
  width: 31px;
  height: 31px;
  position: relative;
  zoom: 1;
  display: inline-block;
  vertical-align: middle;
  margin-right: 5px;
} */
</style>
