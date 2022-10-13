<template>
	<view class="all">
		
		<view class="my-photo">
			<view class="photo"></view>
			<view class="wenzi">郑洪滨</view>
		</view>
		
		<view class="my-head">
			<view class="my-head-item">
				<text class="my-head-wenzi">活跃度</text>
				<text class="my-head-number">88</text>
				<text class="my-head-fuhao">%</text>
			</view>
			
			<view class="line"></view>
			
			<view class="my-head-item">
				<text class="my-head-wenzi">打卡天数</text>
				<text class="my-head-number">8</text>
				<text class="my-head-fuhao">天</text>
			</view>	
		</view>
		
		<view class="my-massage">
			<image class="youjian-span" src="../../static/image/邮件.png"></image>
			<text class="common-wenzi">我的信息</text>
		</view>
		
		<view class="my-second">
			<view class="my-second-item">
				<image class="youjian-span" src="../../static/image/邮件.png"></image>
				<text class="common-wenzi">我的选择表单</text>
			</view>
			<view class="line-heng"></view>
			<view class="my-second-item">
				<image class="youjian-span" src="../../static/image/邮件.png"></image>
				<text class="common-wenzi">优惠券</text>
			</view>
		</view>
		
		<view class="my-third">
			<view class="my-third-item">
				<image class="youjian-span" src="../../static/image/邮件.png"></image>
				<text class="common-wenzi">设置</text>
			</view>
			<view class="line-heng-one"></view>
			<view class="my-third-item">
				<image class="youjian-span" src="../../static/image/邮件.png"></image>
				<text class="common-wenzi">帮助与反馈</text>
			</view>
			<view class="line-heng-two"></view>
			<view class="my-third-item">
				<image class="youjian-span" src="../../static/image/邮件.png"></image>
				<text class="common-wenzi">给我们好评</text>
			</view>
		</view>
		<view-tabbar :current="3"></view-tabbar>
	</view>
	
</template>

<script>
	import Tabbar from '@/components/foot-tabbar/foot-tabbar.vue'
	export default {
		data() {
			return {
				activeclass: 1
			}
		},
		components:{
				'view-tabbar': Tabbar
		},
		onShow() {
		    uni.hideTabBar({
		        animation: false
		    })
		},
		methods: {
			
		}
	}
</script>

<style>
	.all{
		height: 1640rpx;
		width: 750rpx;
		background-color: #eeeeee;
	}
	.my-photo{
		float: left;
		width: 100%;
		height: 200rpx;
		margin-top: 138rpx;
	}
	.photo{
		width: 145rpx;
		height: 145rpx;
		border: 1rpx #9f9f9f solid;
		margin-left: 300rpx;
		background-color: white;
		border-radius: 50%;
	}
	.wenzi{
		margin-top: 23rpx;
		font-size: 25rpx;
		margin-left: 335rpx;
	}
	.my-head{
		float: left;
		margin-left: 49rpx;
		margin-top: 40rpx;
		width: 648rpx;
		height: 96rpx;
		border: 1rpx #9f9f9f solid;
		background-color: #f1f1f1;
		border-radius: 25rpx;
		margin-bottom: 50rpx;
	}
	.my-head-item{
		float: left;
		width: 324rpx;
		height: 48rpx;
	}
	.line{
		position:absolute;
		
		float: left;
		width: 2rpx;
		height: 96rpx;
		margin-left: 323rpx;
		background-color: #9f9f9f;
	}
	.my-head-wenzi{
		float: left;
		
		font-size: 30rpx;
		font-family: '表通体黑';
		margin-top: 30rpx;
		margin-left: 35rpx;
	}
	.my-head-number{
		float: left;
		font-size: 50rpx;
		margin-top: 17rpx;
		margin-left: 70rpx;
	}
	.my-head-fuhao{
		float: left;
		font-size: 37rpx;
		margin-top: 25rpx;	
	}
	.my-massage{
		float: left;
		margin-left: 49rpx;
		margin-top: 20rpx;
		width: 648rpx;
		height: 96rpx;
		border: 1rpx #9f9f9f solid;
		background-color: #ffffff;
		border-radius: 25rpx;
	}
	.youjian-span{
		float: left;
		width: 50rpx;
		height: 45rpx;
		margin-top: 25rpx;
		margin-left: 25rpx;
	}
	.common-wenzi{
		float: left;
		font-size: 29rpx;
		margin-left: 20rpx;
		margin-top: 28rpx;
	}
	.my-second{
		float: left;
		margin-left: 49rpx;
		margin-top: 40rpx;
		width: 648rpx;
		height: 192rpx;
		border: 1rpx #9f9f9f solid;
		background-color: #ffffff;
		border-radius: 25rpx;
	}
	.my-second-item,.my-third-item{
		float: left;
		width: 648rpx;
		height: 96rpx;
	}
	.line-heng,.line-heng-one{
		position:absolute;
		margin-top: 96rpx;
		float: left;
		width: 650rpx;
		height: 1rpx;
		background-color: #9f9f9f;
	}
	.my-third{
		float: left;
		margin-left: 49rpx;
		margin-top: 40rpx;
		width: 648rpx;
		height: 288rpx;
		border: 1rpx #9f9f9f solid;
		background-color: #ffffff;
		border-radius: 25rpx;
	}
	.line-heng-two{
		position:absolute;
		margin-top: 192rpx;
		float: left;
		width: 650rpx;
		height: 1rpx;
		background-color: #9f9f9f;
	}
</style>
