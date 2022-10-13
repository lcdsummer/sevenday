<template>
	<view class="second">
	<view class="search-head">
	<view class="phone-search">
		<image class="search-span" src="../../static/image/searchSpan.png"/>
		<input type="text" placeholder="请输入您要查找的手机号" placeholder-style="color:#dadada"/>
	</view>
	<text class="quxiao">取消</text>
	</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		},
	}
</script>

<style scoped>
	.second{
		width: 750rpx;
		height: 1625rpx;
		background-color: #EEEEEE;
	}
	.search-head{
		display: flex;
		height: 165rpx;

	}
	.search-span{
		width: 40rpx;
		height: 40rpx;
		margin-top: 12rpx;
		margin-left: 20rpx;
	}
	.phone-search{
		display: flex;
		height: 60rpx;
		width: 595rpx;
		margin-top: 99rpx;
		margin-left: 39rpx;
		border: 1px #4678FA solid;
		background-color: white;
		border-radius: 50rpx;
	}
	
	.phone-search input{
		font-size: 25rpx; 
		margin-top: 14rpx;
		margin-left: 100rpx;
	}

	.quxiao{
		font-size: 25rpx;
		font-family: "标题黑";
		font-weight: bold;
		margin-top: 112rpx;
		margin-left: 30rpx;
		color: #4678FA;
	}
</style>
