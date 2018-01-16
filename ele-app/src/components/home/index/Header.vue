<template>
	<header class='header'>
		首页
	</header>
</template>

<script>
	export default{
		name:'home-header',
	}
</script>

<style>
	.header{
		width:100%;
		height:80px;
		line-height:30px;
		color:#fff;
		background:linear-gradient(90deg,#0af,#0085ff)
	}
	.header:after{
		width:100%;
		height:1px;
		position:absolute;
		bottom:-1px;
		left:0px;
		border-bottom:1px solid #999;
		transfrom:scaleY(0.5);
		z-index:1;
	}
</style>