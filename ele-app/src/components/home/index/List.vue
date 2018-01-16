<template>
	<ul class='lists'>
		<li class='list' v-for='(item,index) in dataList' >
			<router-link :to='"/home/detail/"+item+"/"+index'>{{item}}</router-link>
		</li>
	</ul>
</template>

<script>
	export default {
		name:'home-list',
		data(){
			return {
				dataList:['1','2','3','4','5','6','7','8','9','10']
			}
		},
		created(){
			this.$event.$on('modify-index',(obj)=>{
				console.log(obj)
				console.log(obj.item)
				this.dataList.splice(obj.index,1,obj.item);
			})
		}
	}
</script>

<style>
	.lists .list{
		height:40px;
		padding-left:20px;
		line-height:40px;
		width:100%;
		border-bottom:1px solid #fff;
		background:#FFC0CB;
	}
</style>