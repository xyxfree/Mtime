<template>
  <div class="imgMask">
    <a class="prev"  @click.stop="prev"><</a>
    <div class="showImg" >
      <img class="bigImg" :src="data.imgList[num].mage">
    </div>
    <a class="next"  @click.stop="next">></a>
    <span class="hot">正在热映</span>
    <span class="movie-name" >{{data.imgList[num].name}}</span>
    <span class="brief">{{data.imgList[num].brief}}</span>
    <span class="introduction">{{data.imgList[num].introduction}}</span>
    <a class="details" :href="data.imgList[num].address">
        <span class="fang"></span>查看详情</a>
    </div>
</template>
<script>
import data from '../data.js'
  export default {
    data() {
      return{
        num:0,
        data
      }
    },
    methods:{
        prev(){
            if(this.num==0){
                this.num =2
            }
            this.num--;
        },
        next(){
            if(this.num==1){
                this.num=-1;
            }
            this.num++;
        }
    }
  }
</script>
<style>
.prev,.next{
		position:absolute;
		font:60px/80px '微软雅黑';
		cursor: pointer;
		top:155px;
		width: 49px;
		height: 104px;
    padding-top:10px;
		background-color: rgba(17, 16, 16,0.4);
		text-align: center;
	}
.prev{
  left: 60px;
  border-radius: 8px 0 0 8px;
}
.next{
  right: 60px;
  border-radius: 0 8px 8px 0;
}
.prev:hover{
  color: antiquewhite;
}
.next:hover{
  color: antiquewhite;
}
.showImg{
  height: 390px;
}
.bigImg{
  width: 100%;
  height: 390px;
}
.imgMask{
  position: relative;
  padding-top:60px;
}
.hot,.movie-name,.brief,.introduction,.details{
  position: absolute;
  left: 125px;
  padding: 5px 10px;
  margin-bottom: 5px;
  color: #fff;
}
.hot{
  top:140px;
  font-size: 14px;
  background: #ff6d00;
}
.movie-name{
  top:180px;
  font-size: 30px;
  width: 600px;
}
.brief{
  top:240px;
  width: 600px;
  font-size: 16px;
}
.introduction{
  top:290px;
  font-size: 16px;
  width: 600px;
}
.details{
  top:330px;
  font-size: 14px;
  text-decoration: none;
}
.fang{
  display: inline-block;
  width: 6px;
  height: 10px;
  border:1px solid white;
  margin-top: 2px;
  margin-right: 5px;
  }
</style>
