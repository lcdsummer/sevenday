<template>
	<view class="five">
		
		<view class="top">
			<firsthead title=""></firsthead>
		</view>
		
		<view class="logo-photo">
			<image src="../../static/image/logo.png"></image>
		</view>
		<view class="passage">
			
			<view class="item">
				<view class="select-left">软件名</view>
				<view class="select">少年代码</view>		 
			</view>
			
			<view class="item">
				<view class="select-left">版本号</view>
				<view class="select">shaoniandaima1.0</view>	 
			</view>
			
			<view class="item">
				<view class="select-left">版本更新</view>
				<i class="iconfont icon-youjiantou-copy"></i> 
			</view>
			
			<view class="item">
				<view class="select-left">开发团队</view>
				<view class="select">南方少年工作室</view>	 
			</view>
			
			<view class="item">
				<view class="select-left">合作伙伴</view>
				<i class="iconfont icon-youjiantou-copy"></i>
			</view>
			
		</view>
		
		<view class="foot">
		<text>《用户协议》</text><text>|</text><text>《隐私协议》</text>
		</view>


	</view>
</template>

<script>
	import firsthead from '../../components/firsthead/firsthead.vue'
	export default {
		data() {
			return {
			}
		},
		components : {
			firsthead
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	
	.five{
		width: 750rpx;
		height: 1625rpx;
		background-color: #EEEEEE;
	}
	.logo-photo{
		margin-left: 100rpx;
		width: 550rpx;
		height: 370rpx;
		text-align: center;
		border-bottom: solid 1rpx #e3e3e3;
	}
	.logo-photo image{
		width: 135rpx;
		height: 135rpx;
		margin-top: 100rpx;
	}
	.item{
		height: 100rpx;
		width: 550rpx;
		line-height: 80rpx;
		margin-left: 100rpx;
		float: left;
		border-bottom: solid 1rpx #e3e3e3;
	}

	.passage{
		background-color: #eee;
		margin-top: 10rpx;
		width: 100%;
		height: 530rpx;
		
	}
	
	.select-left{
		margin-top: 15rpx;
		float: left;
	}
	
	.iconfont{
		margin-top: 18rpx;
		float: right;
		color: #707070;
	}
	.select{
		margin-top: 20rpx;
		float: right;	
		text-align: right;
		color: #707070;
	}

	.foot{
		margin-top: 430rpx;
		text-align: center;
	}
	.foot text{
		color: #064389;
	}
</style>
