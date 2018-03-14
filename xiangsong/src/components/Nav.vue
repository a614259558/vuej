<template>
	<div id="app">
		<ul id="nav">
			<li class="change">
				<i class="iconfont icon-richu"></i>
				<span>当日面包</span>
			</li>
			<li>
				<i class="iconfont icon-canting"></i>
				<span>蛋糕西点</span>
			</li>
			<li>
				<i class="iconfont icon-icon-test1"></i>
				<span>饮品小食</span>
			</li>
			<li>
				<i class="iconfont icon-tuangou"></i>
				<span>团购充值</span>
			</li>
		</ul>
		<ul id="indexList">
			<!-- <li>
				<a href="javascript:;">
					<img src="../../static/img/l1-1.jpg" alt="">
				</a>
				<div class="productInfo">
					<div class="left">
						<h2 class="pName">芝士双莓杯装蛋糕</h2>
						<p class="PIntroduce">80g/瓶</p>
						<p class="good"><i class="iconfont icon-xinyi"></i>&nbsp;81.25%</p>
					</div>
					<div class="right">
						<p class="price">
							<span>￥30.00</span><em>￥</em><b>25.00</b>
						</p>
						<p class="pNumber">
							<i class="addone iconfont icon-jia2"></i>
						</p>
					</div>
				</div>
			</li> -->
			<li v-for="item in list">
				<a href="javascript:;">
					<!-- 将l1-1.jpg替换为item.imgsrc -->
					<!-- <img src="../../static/img/l1-1.jpg" alt=""> -->
					<img :src="item.imgsrc" alt="">
				</a>
				<div class="productInfo">
					<div class="left">
						<h2 class="pName">{{item.pname}}</h2>
						<p class="PIntroduce">{{item.jieshao}}</p>
						<p class="good"><i class="iconfont icon-xinyi"></i>&nbsp;{{item.pgood}}</p>
					</div>
					<div class="right">
						<p class="price">
							<span>{{item.oldprice}}</span><em>￥</em><b>{{item.nowprice}}</b>
						</p>
						<p class="pNumber">
							<i class="addone iconfont icon-jia2"></i>
						</p>
					</div>
				</div>
			</li>
		</ul>
		<div id="liubai">
			
		</div>
	</div>
</template>

<script>
	import axios from 'axios';

	export default {
  		name: 'Nav',
  		data(){
  			return{
  				list:{}
  			}
  		},
		mounted() {
			axios.get("../../static/json/index.json")
			.then((res)=>{
				this.list = res.data.list1;
				var that = this;
				$("#nav").on("click","li",function(){
					$(this).addClass("change")
						   .siblings().removeClass("change");
					console.log(that);
					// for( var attr in res ){
					// 	if( attr.split("").pop() == $(this).index() ){
					// 		that.list = res.data.attr
					// 		console.log( that.list.data )
					// 	}
					// }
				})
			})
		}
	}
</script>

<style scoped>
	/*#app{
		height:.69rem;
	}*/
	#nav{
		height:.69rem;
		width:96%;
		padding-top:.1rem;
		margin:0 auto;
		display:flex;
	}
	#nav>li{
		height:100%;
		width:.9rem;
		display:flex;
		flex-direction:column;
		justify-content:center;
		align-items:center;
	}
	#nav>li>i{
		font-size:.2rem;
		line-height:.3rem;
		color:#e6423e;
		width:.3rem;
		height:.3rem;
		border-radius:50%;
		text-align:center;
	}
	#nav>li>span{
		font-size:.12rem;
		color:#555b6b;
	}

	#indexList>li{
		height:3.54rem;
		margin-bottom:.05rem;
		display:flex;
		flex-direction:column;
	}
	#indexList>li>a{
		height:2.5rem;
	}
	#indexList>li>a>img{
		width:100%;
		height:100%;
	}
	.productInfo{
		flex:1;
		display:flex;
	}
	.productInfo>div{
		width:50%;
	}
	.left{
		text-align:left;
		padding-left:.14rem;
		color:#555B6B;
	}
	.right{
		text-align:right;
	}
	.pName{
		font-size:.16rem;
		margin:.05rem 0 .1rem;
	}
	.PIntroduce{
		font-size:.11rem;
	}
	.good{
		color:#BCBBC4;
		margin:.05rem 0 .15rem 0;
	}
	.price{
		font-size:.12rem;
		color:#BCBBC4;
	}
	.price>span{
		text-decoration:line-through;
	}
	.price>b{
		font-size:.18rem;
		color: #555B6B;
	}
	.pNumber>span{
		font-size:.2rem;
		line-height:.28rem;
		font-weight:900;
		margin-right:.1rem;
	}
	.addone{
		width:.28rem;
		height:.28rem;
		font-size:.2rem;
		line-height:.2rem;
		text-align:center;
		border-radius:50%;
		color:white;
		background:red;
	}
	.change{
		border-bottom:.02rem solid red;
	}
	.change>i{
		background:red;
		color:white!important;
	}

	#liubai{
		height:.69rem;
	}
</style>