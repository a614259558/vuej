<template>
	<div id="app">
		<header>
			<img src="../../static/img/logo.png" alt="">
			<div class="adr">
				<span>配送至：<em>香送</em></span>
				<i class="iconfont icon-gengduo"></i>
			</div>
		</header>
	</div>
</template>

<script>
	export default {
	  name: 'CommonHead',
	}
</script>

<style scoped>
	header{
		height:.5rem;
		padding:.1rem 0;
	}
	header img{
		float:left;
		height:.3rem;
		width:auto;
		margin:0 .15rem;
	}
	.adr{
		float:left;
		width:2.4rem;
		height:.3rem;
		border-radius:.15rem;
		background:#EFEFF4;
		font-size:.14rem;
		line-height:.3rem;
		color:#4b4b4b;
		padding:0 .14rem;
		display:flex;
		justify-content:space-between;
	}
</style>