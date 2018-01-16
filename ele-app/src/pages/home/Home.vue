<template>
	<div>
		
	<page pageId='home' >
		<home-header></home-header>
		<home-banner></home-banner>
		<home-list></home-list>
	</page>
	<!--装载子页面-->
	<transition enter-active-class='slideInRight ani' leave-active-class='slideOutRight ani'> 
	<router-view></router-view>
	</transition>
	</div>
</template>

<script>
	import Page from '../../common/Page.vue'
	import Banner from '../../components/home/index/Banner.vue'
	import Header from '../../components/home/index/Header.vue'
	import List from '../../components/home/index/List.vue'
	export default {
		
		components:{
			[Banner.name]:Banner,
			[Header.name]:Header,
			[List.name]:List,
			[Page.name]:Page,
		}
	}
</script>

<style scoped>
	.ani{
	    animation-duration: 300ms;
	    animation-timing-function: ease-in;
	}
</style>