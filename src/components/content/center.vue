<template>
  <div class="color">
    <div class="cf">
      <a target="_blank" href="http://feature.mtime.com/2018/249092/ticket/index.html#290"><img width="1000" :src="pic" alt=""></a>
    </div>
    <div class="content">
      <div class="titles clearfix">
        <h2>正在热映<span>{{data.datas.length}}</span>部</h2>
        <div class="filelink">
          <a href="javascript:" v-if="shrink" @click="toggleClick">全部</a>
          <a href="javascript:" v-if="!shrink">全部</a>
          <a href="javascript:" v-if="!shrink" @click="small('3D')">3D</a>
          <a href="javascript:" v-if="shrink" @click="small1('3D')">3D</a>
          <a href="javascript:" v-if="!shrink" @click="large('中国巨幕')">IMAX</a>
          <a href="javascript:" v-if="shrink" @click="large1('中国巨幕')">IMAX</a>
          <a href="javascript:" v-if="!shrink" @click="joke('喜剧')">喜剧</a>
          <a href="javascript:" v-if="shrink" @click="joke1('喜剧')">喜剧</a>
          <a href="javascript:" v-if="!shrink" @click="joke('奇幻')">奇幻</a>
          <a href="javascript:" v-if="shrink" @click="joke1('奇幻')">奇幻</a>
          <a href="javascript:" v-if="!shrink" @click="joke('动作')">动作</a>
          <a href="javascript:" v-if="shrink" @click="joke1('动作')">动作</a>
          <a href="javascript:" v-if="!shrink" @click="joke('爱情')">爱情</a>
          <a href="javascript:" v-if="shrink" @click="joke1('爱情')">爱情</a>
          <a href="javascript:" v-if="!shrink" @click="joke('冒险')">冒险</a>
          <a href="javascript:" v-if="shrink" @click="joke1('冒险')">冒险</a>
        </div>
      </div>
      <div class="moviebox clearfix">
        <div class="firstmovie" :class="{'main-hide-text': shrink}">
          <dl>
            <dt>
              <img width="270" :src="mage" alt="">
            </dt>
            <dd>
              <div class="score">
                <dfn>总评分</dfn>
                <p>6.1</p>
              </div>
              <h2>
                <a target="_blank" href="http://movie.mtime.com/223926/">移动迷宫3：死亡解药</a>
              </h2>
              <h3>
                142分钟 -
                <a target="_blank" href="http://movie.mtime.com/movie/search/section/?type=Action#type=185">动作</a>
                /
                <a target="_blank" href="http://movie.mtime.com/movie/search/section/?type=Sci-Fi#type=193">科幻</a>
              </h3>
              <p class="hotmovie">
                跑男团"探寻迷宫共赴龙潭虎穴
              </p>
              <div class="moviebtn">
                <strong>28</strong>元起
                <a target="_blank" href="http://theater.mtime.com/China_Beijing/movie/223926/">选座购票</a>
              </div>
            </dd>
          </dl>
        </div>
        <div class="othermovie">
          <ul class="xi" :class="{'main-hide-input': show}">
            <li v-for="item in data.datas" v-show="item.bool">
              <a href="javascript:" class="picbox">
                <img :src="item.address" alt="">
                <span class="scored">{{item.rating}}</span>
                <span class="banben">
                  <strong>{{item.small}}</strong>
                  <i>{{item.large}}</i>
                </span>
              </a>
              <dl>
                <dt>
                  <a :href="item.nameaddress" class="movietitle">{{item.name}}</a>
                </dt>
                <dd class="ad">
                  {{item.runtime}}
                  <a :href="item.address1">{{item.genres1}}</a>
                    /
                  <a :href="item.address2">{{item.genres2}}</a>
                </dd>
                <dd>{{item.price}}</dd>
                <dd class="hotted">{{item.title}}</dd>
                <dd class="top">
                  <a class="buy" :href="item.buy">选座购票</a>
                </dd>
              </dl>
            </li>
          </ul>
          <div v-show="none" v-if="!show" class="more" @click="take">
            <i></i>
            更多</div>
          <div v-show="none" v-if="show" class="mored" @click="take1">
          <i></i>收回</div>
        </div>
      </div>
    </div>
	</div>
</template>
<script>
import data from '../data.js'
import mage from './mage.jpg'
import pic from './pic.jpg'
    export default {
        data() {
          return{
            data,
            mage,
            pic,
            show:false,
            shrink: false,
            none:true,
          }
        },
        methods:{
          toggleClick () {
            this.none= !this.none;
            this.shrink = !this.shrink;
              this.data.datas.filter(function (item) {
                item.bool=true;
            })
          },
          joke (key) {
            this.shrink = !this.shrink;
              this.none= false;
            this.data.datas.filter(function (item) {
              item.bool=true;
              if (item.genres1!==key&&item.genres2!==key) {
                    item.bool=false;
                }
            })
          },
          small (key) {
            this.shrink = !this.shrink;
              this.none= false;
            this.data.datas.filter(function (item) {
              item.bool=true;
              if (item.small!==key) {
                    item.bool=false;
                }
            })
          },
           large (key) {
            this.shrink = !this.shrink;
              this.none= false;
            this.data.datas.filter(function (item) {
              item.bool=true;
              if (item.large!==key) {
                    item.bool=false;
                }
            })
          },
          joke1 (value) {
            this.shrink = this.shrink;
            this.data.datas.filter(function (item) {
              item.bool=true;
              if (item.genres1!==value&&item.genres2!==value) {
                    item.bool=false;
                }
            })
          },
          small1 (value) {
            this.shrink = this.shrink;
            this.data.datas.filter(function (item) {
              item.bool=true;
              if (item.small!==value) {
                    item.bool=false;
                }
            })
          },
         large1 (value) {
            this.shrink = this.shrink;
            this.data.datas.filter(function (item) {
              item.bool=true;
              if (item.large!==value) {
                    item.bool=false;
                }
            })
          },
          take () {
            this.show= !this.show;
          },
           take1 () {
            this.show= !this.show;
          }
        }
    }
</script>


<style>
a{
  cursor:pointer;
}
img{
  border:none;
}
.more,.mored{
  color: #333;
  position: absolute;
  bottom:30px;
  left: calc(50% - 36px);
  cursor: pointer;
}
.more i,.mored i{
  background: url(//static1.mtime.cn/theater/20170719092733/images/allicon24.png) no-repeat -267px -336px;
  width: 31px;
  height: 31px;
  position: relative;
  zoom: 1;
  display: inline-block;
  vertical-align: middle;
  margin-right: 5px;
}
.mored i{
  background: url(//static1.mtime.cn/theater/20170719092733/images/allicon24.png) no-repeat -267px -303px;
}
dl,dd,h2,h3,p{
  margin:0;
}
.color{
  background: #f2f2f2;
  padding-top:40px;
}
.cf{
  width: 1000px;
  margin: 0 auto;
}
.cf a{
  display: inline-block;
  margin-bottom: 15px;
}
.content{
  width: 1000px;
  margin: auto;
  background: #f2f2f2;
}
.titles{
  border-bottom: 1px solid #a9a9a9;
}
.clearfix:after {
  content: ".";
  height: 0;
  visibility: hidden;
  display: block;
  clear: both;
}
.titles h2{
  margin: 0;
  float: left;
  width: 180px;
  font-size: 20px;
  font-weight: normal;
  line-height: 48px;
  border-left: 10px solid #ff6d00;
  padding: 0 15px;
}
.titles h2 span{
  font-size: 36px;
  padding: 0 8px;
  color: #333;
}
.filelink{
  width: 500px;
  font-size: 14px;
  line-height: 24px;
  margin-top: 15px;
  float: left;
}
.filelink a{
  display: inline-block;
  font-size: 14px;
  line-height: 24px;
  cursor: pointer;
  text-decoration: none;
  padding-right:10px;
}
.moviebox{
  padding-top: 20px;
  position: relative;
  padding-bottom:80px;
}
.firetmovie{
  width: 272px;
  float: left;
}
dd{
  position: relative;
}
.score{
  background: #669c20;
  color: #fff;
  width: 52px;
  height: 52px;
  position: absolute;
  left: 0;
  top: 0;
  text-align: center;
  font: 12px/150% helvetica,"微软雅黑";
}
.score dfn{
  font-size: 12px;
  line-height: 1em;
  padding: 8px 0 4px;
  display: block;
  font-style: normal;
  font-weight: normal;
}
.score p{
  font-size: 24px;
}
dd h2{
  font-size: 20px;
  font-weight: normal;
  padding-left: 65px;
}
dd h2 a{
  font-size: 20px;
  font-weight: normal;
  text-decoration: none;
  color: #333;
}
.firstmovie dd h3 {
  font-size: 14px;
  line-height: 24px;
  padding-left: 65px;
    font-weight: normal;
}
.firstmovie dd h3 a {
  margin: 0 5px;
  color: #333;
  text-decoration: none;
}
.firstmovie dd .hotmovie {
  color: #679c21;
  font-size: 18px;
  line-height: 26px;
  padding: 0 0 10px 30px;
  margin: 10px 0 0;
  position: relative;
  zoom: 1;
}
.firstmovie{
  float: left;
  margin-right: 48px;
}
.moviebtn{
  text-align: right;
}
.moviebtn strong{
  font-size: 54px;
  line-height: 1em;
  margin-right: 6px;
  color: #333;
}
.firstmovie .moviebtn a {
  text-decoration: none;
  display:inline-block;
  width: 162px;
  height: 46px;
  text-align: center;
  border-radius: 40px;
  margin-left: 10px;
  background-color: #08c;
  color: white;
  font-size: 24px;
  line-height: 46px;
  letter-spacing: 2px;
  cursor: pointer;
}
.top{
  margin-top: 8px;
}
.othermovie .xi{
  padding: 0;
  margin: 0;
  list-style: none;
  overflow: hidden;
  height: 567px;
}
.xi .buy{
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
  .xi .buy:hover{
  background-color: red;
  }
.othermovie .main-hide-input{
  overflow: inherit;
}
.othermovie li{
  width: 320px;
  zoom: 1;
  margin: 0 0 45px 10px;
  float: left;
}
.picbox{
  width: 102px;
  margin-right: 13px;
  position: relative;
  float: left;
  display: inline;
}
.xi .ad a:hover{
  color: #08c;
}
.picbox .scored{
  background: #679c21;
  font-size: 14px;
  line-height: 20px;
  color: #fff;
  height: 20px;
  padding: 0 5px;
  position: absolute;
  bottom: -5px;
  right: -5px;
}
.picbox .banben{
  width: 37px;
  position: absolute;
  right: 5px;
  top: 5px;
}
.banben strong{
  padding: 2px 4px;
  background-color: rgba(24, 23, 23, 0.41);
  color: #fff;
  border: 1px solid white;
  border-radius: 5px;
}
.banben i{
  width: 37px;
  height: 44px;
  background-color: rgba(24, 23, 23, 0.41);
  color: #fff;
  margin-top: 5px;
  display: inline-block;
  position: relative;
  zoom: 1;
  overflow: hidden;
  font-style: normal;
  font-weight: normal;
}
.firstmovie h2 a:hover{
  color: #08c;
}
.firstmovie h3 a:hover{
  color: #08c;
}
.othermovie li dl {
  width: 205px;
  float: left;
  display: inline;
}
.othermovie li dt {
  font-size: 18px;
  line-height: 24px;
  padding-bottom: 8px;
}
.movietitle{
  font-size: 18px;
  line-height: 24px;
  color: #333;
}
.movietitle:hover{
  color: #08c;
}
.othermovie li dd {
  font-size: 14px;
  line-height: 24px;
}
.othermovie li dd a {
  margin: 0 5px;
}
.othermovie li dl a {
  color: #333;
	text-decoration: none;
}
.othermovie li .hotted {
  color: #679c21;
  line-height: 20px;
  margin: 10px 0 0;
  white-space :nowrap;
  overflow: hidden;
}
.main-hide-text{
  display: none;
}
.main-hide-input{
   overflow: inherit;
}
</style>
