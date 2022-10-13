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
		height: 150rpx;
		width: 750rpx;
		font-size: 28rpx;
		line-height: 150rpx;
		text-align: center;
		position: relative;
		}
	.head-left{
		position:absolute;
		float: left;
		margin-left: 50rpx;
		text-align: center;
	    }

</style>