<template>
	<div class='page' :id='pageId' ref='page'>
		<div class='wrapper'>
			<slot></slot>
		</div>
	</div>
</template>

<script>
	import Iscroll from 'iscroll'
	console.log(Iscroll)
	export default {
		name:'page',
		props:{
			pageId:String,
		},
		data(){
			return{
				
			}
		},
		mounted(){
			let scroll = new Iscroll(this.$refs.page,{
				bounce:true,
			})
		}
	}
</script>

<style>
	.page{
		width:100%;
		position:absolute;
		left:0;
		top:0;
		bottom:49px;
		overflow:hidden;
	}
</style>