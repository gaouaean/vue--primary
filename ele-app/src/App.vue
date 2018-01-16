<template>
  <div id="app">
    <keep-alive>
    	<router-view></router-view>
   	</keep-alive>
   <tabs></tabs>
  </div>
</template>

<script>
	import Tabs from './common/Tabs.vue'
export default {
  components:{
  	[Tabs.name]:Tabs
  }
}
</script>

<style>
#app,html,body{
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
	width:100%;
	height:100%;
	touch-action:none;
}

</style>
