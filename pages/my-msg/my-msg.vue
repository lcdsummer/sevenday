<template>
	<view class="five">
		
		<view class="top">
			<firsthead title="个人信息"></firsthead>
		</view>
		
		<view class="passage">
			
			<view class="item">
				<view class="select-left">头像</view>
				<view class="photo"></view>	 
			</view>
			
			<view class="item">
				<view class="select-left">昵称</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select">小郑</view>	 
			</view>
			
			<view class="item">
				<view class="select-left">性别</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select">男</view>	 
			</view>
			
			<view class="item">
				<view class="select-left">生日</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select">2001.09.20</view>	 
			</view>
			
			<view class="item">
				<view class="select-left">地区</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select">广东省黄埔区</view>	 
			</view>
			
			<view class="item">
				<view class="select-left">个人简历</view>
				<i class="iconfont icon-youjiantou-copy"></i>
			</view>
			
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
			bindPickerChange(e){
				this.index=e.detail.value
			},
			
			
		}
	}
</script>

<style lang="scss">
	
	.five{
		width: 750rpx;
		height: 1625rpx;
		background-color: #EEEEEE;
	}

	.item{
		height: 80rpx;
		width: 640rpx;
		line-height: 80rpx;
		margin-left: 65rpx;
		float: left;
		
	}

	.passage{
		background-color: #EEEEEE;
		margin-top: 20rpx;
		width: 100%;
		height: 530rpx;
		
		
	}
	
	.select-left{
		margin-top: 15rpx;
		float: left;
	}
	
	.iconfont{
		margin-top: 18rpx;
		margin-left: 15rpx;
		float: right;
		color: #a9a9a9;
	}
	.select{
		margin-top: 20rpx;
		margin-left: 250rpx;
		width: 180rpx;
		float: right;	
		text-align: right;
		color: #a9a9a9;
	}
	.photo{
		background-color: white;
		border: 1rpx #a9a9a9 solid;
		border-radius: 50%;
		width: 68rpx;
		height: 68rpx;
		float: right;	
		margin-top: 20rpx;
		margin-left: 250rpx;
	}
	
	

</style>
