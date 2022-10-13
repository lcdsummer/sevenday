<template>
	<view class="first-head">
	<view class="head-left">
	<i class="iconfont icon-zuojiantou-copy"></i>
	</view>
	{{title}}
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		props : ['title']
	}
</script>

<style scoped>
	.first-head{
		height: 100rpx;
		width: 750rpx;
		font-size: 28rpx;
		line-height: 150rpx;
		text-align: center;
		background-color: #eee;
		position: fixed;
		z-index: 100;
		top: 0%;
		}
	.head-left{
		
		margin-left: 50rpx;
		text-align: center;
		position: fixed;
		z-index: 100;
	    }

</style>