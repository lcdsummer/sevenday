<template>
	<view class="second">
		
	<view class="search-head">
	<view class="phone-search">
		<image class="search-span" src="../../static/image/searchSpan.png"/>
		<input type="text" placeholder="请输入您要查找的手机号" placeholder-style="color:#dadada"/>
	</view>
	<text class="quxiao">取消</text>
	</view>
	
	<view class="user">
		<view class="photo">
			<open-data type="userAvatarUrl" class="userinfo" id="userinfo">
			<image src="../../static/image/头像.jpg" mode="widthFix"></image>
			</open-data>
		</view>
		<view class="name">ZHANGSAN</view>
		<view class="area">广东-汕头</view>
		
	</view>
	
	<view class="user">
		<view class="photo">
			<open-data type="userAvatarUrl" class="userinfo" id="userinfo">
			<image src="../../static/image/头像.jpg" mode="widthFix"></image>
			</open-data>
		</view>
		<view class="name">LISI</view>
		<view class="area">广东-湛江</view>
		
		
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
	
	.user{
		width: 670rpx;
		height: 130rpx;
		background-color: white;
		float: left;
		margin-top: 50rpx;
		margin-left: 39rpx;
		border-radius: 20rpx;
	}
	
	#userinfo{
	  width: 90rpx;
	  height:90rpx;
	  border-radius:50%;
	  display: flex;
	  overflow:hidden;
	  float: left;
	  margin-top: 20rpx;
	  margin-left: 50rpx;
	}
	.name{
		float: left;
		height: 30rpx;
		margin-top: 30rpx;
		margin-left: 20rpx;
	}
	.area{
		font-size: 20rpx;
		color: #acacac;
		margin-left: 160rpx;
		margin-top: 70rpx;
	}
</style>
