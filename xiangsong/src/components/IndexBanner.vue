<template>
	<div id="app">
		<div class="swiper-container" id="banner">
		    <div class="swiper-wrapper">
		        <div class="swiper-slide slide1">
		        	<img src="../../static/img/banner1.jpg" alt="">
		        </div>
		        <div class="swiper-slide slide2">
		        	<img src="../../static/img/banner2.jpg" alt="">
		        </div>
		        <div class="swiper-slide slide3">
		        	<img src="../../static/img/banner3.jpg" alt="">
		        </div>
		    </div>
		    <!-- 如果需要分页器 -->
		    <div class="swiper-pagination"></div>
		</div>
	</div>
</template>

<script>
	export default {
	  name: 'IndexBanner',
	  mounted(){
	 //  	var mySwiper = new Swiper('.swiper-container', {
		// 		autoplay:  {
		// 			stopOnLastSlide:true,
		// 		},
		// 		pagination: {
		// 			el: '.swiper-pagination',
		// 			bulletElement: 'span',
		// 			clickable: true,
		// 			// 如果需要分页器
		// 		    pagination: {
		// 		      el: '.swiper-pagination',
		// 		    },
		// 		}
		// })
			var mySwiper = new Swiper ('.swiper-container', {
					loop: true,
					autoplay: true,
					pagination: {
				      el: '.swiper-pagination',
				    }
			}) 
	  }
	}
	  
</script>

<style scoped>
	#banner{
		height:1.75rem;
		width:3.75rem;
	}
	#banner img{
		width:100%;
		height:100%;
	}
	.swiper-wrapper{
		position:relative;
	}
	.swiper-slide{
		height:1.75rem;
		width:3.75rem;
	}/*
	.slide1{
		position:absolute;
		top:0;
		left:0;
	}
	.slide2{
		position:absolute;
		top:0;
		left:3.75rem;
	}
	.slide3{
		position:absolute;
		top:0;
		left:7.5rem;
	}*/
</style>