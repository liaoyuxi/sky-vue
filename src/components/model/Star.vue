<template>
	<div class="stars">
		<div v-show="!!num">
			
			<span class="iconfont" v-for="(item,index) in 5" :class="[number(num)> index?'icon-11-copy':'icon-star']"></span>
			<span>{{num+'分'}}</span>
		</div>
		<div class="star-col" v-show="!!!num">暂无评分</div>
	</div>
</template>
<script type="text/javascript">
	export default {
		props:['num'],
		methods:{
			number:function(num){
				
				return  Math.floor(num/2)%5;
			}
		}
	}
</script>
<style lang="scss">
	.stars{
		margin:0 auto;
		line-height:.2rem;
		font-size:.12rem;
		
		.iconfont{
			font-size:inherit;
			color:#f4ea2a;
		}
	}
</style>