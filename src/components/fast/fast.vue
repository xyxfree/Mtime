<template>
<div class="upcoming">
    <div class="titles">
      <h2>即将上映 －1月19日~2月2日</h2>
    </div>
		<div class="upcomingRegion">
				<a class="upcomingprev" @click="changeleft" v-if="show"><</a>
				<a class="upcomingnext" @click="changeright">></a>
			<div class="upcomingSlide clearfix" :style="{left:move +'px'}">
					<dd v-for="item  in data.movieList">
						<ul>
							<li>
								<i></i>
							</li>
							<li class="day">
								<strong>{{item.date}}</strong>
								即将上映
							</li>
							<li class="wantmovie">
								<img :src="item.mage" alt="">
								<div class="upcoming-title">
									<h3>{{item.name}}</h3>
									<p class="one">
										<span>{{item.people}}人想看 - </span>
										<span>{{item.type1}}</span>
										<span>{{item.type2}}</span>
									</p>
									<p class="top">
										<b>导演：</b>
										<span>{{item.actor}}</span>
									</p>
									<p>
										<span>预告片</span>
									</p>
								</div>
							</li>
						</ul>
					</dd>
			</div>
		</div>
</div>
</template>
<script>
import data from '../data.js'
export default {
    data() {
			return {
         move:0,
         data,
         show:false
      }
    },
    methods:{
      changeright (){
        this.move -= 600;
        if (this.move < -295*(data.movieList.length-1)) {
          this.move = -295*(data.movieList.length-1)
        }
        this.show = true;
			},
			changeleft (){
        this.move += 600;
        if (this.move>0) {
          this.move = 0
        }
			}
    }
}
</script>
<style scoped>
 @import "./css/fast.css";
/* .upcoming{
	width: 1000px;
  margin: auto;
	padding: 45px 0 30px 0;
	overflow: hidden
}
.upcoming .titles{
	border-bottom: none;
	height: 48px;
}
.upcoming .titles h2{
	width: 100%;
}
.upcomingRegion{
	position: relative;
	border-top: 2px dashed #f5efef;
    margin-top: 25px;
}
.upcomingSlide{
	width: 15339px;
	left: 0px;
	position: relative;
	transition: .6s all;
}
.upcomingSlide dd{
	width: 295px;
    float: left;
    display: inline;
    margin-right: 16px;
}
.upcomingSlide i{
	position: relative;
    overflow: hidden;
    margin-top: -10px;
	width: 17px;
	height: 17px;
	background-color: white;
	border: 2px solid red;
	border-radius: 50%;
	display: block;
	font-style: normal;
    font-weight: normal;
}
.day{
	color: #7b7b7b;
    font-size: 14px;
    margin-top: 10px;
}
.day strong{
	font-size: 20px;
    line-height: 1em;
	font-weight: normal;
	color: #7b7b7b;
}
.wantmovie{
	position: relative;
    zoom: 1;
    padding-left: 117px;
    min-height: 152px;
    min-height: 152px;
    color: #323232;
    font-size: 14px;
    margin-top: 17px;
}
.wantmovie img{
	display: inline-block;
	position: absolute;
	left: 0;
    top: 0;
}
.upcoming-title h3{
    padding-top: 7px;
    font-size: 16px;
    font-weight: normal;
}
.upcoming-title p{
   margin-top: 6px;
}
.top{
	position: relative;
    padding-left: 45px;
	line-height: 1.5em;
}
.top b{
	position: absolute;
    left: 0;
    top: 0;
    width: 45px;
}
.upcomingprev,.upcomingnext{
	width: 24px;
  height: 59px;
	text-align: center;
	font-size: 34px;
	display: inline;
	z-index: 5;
  background-color: rgb(235, 222, 222);
  padding-top: 5px;
  position: absolute;
  top: 50%;
	margin-top: -30px;
	top:50%;
	cursor:pointer;
}
.upcomingprev{
  left: 0;
  border-radius: 5px 0 0 5px;
}
.upcomingnext{
  right: 0;
  border-radius:  0 5px 5px 0;
} */
</style>
