<template>
	<view class="five">
		
		<view class="top">
			<firsthead title="账号安全"></firsthead>
		</view>
		
		<view class="passage">

			<view class="item">
				<view class="select-left">手机号</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select"><input type="text" v-model="phone"/></view>	 
				
			</view>
			<view class="item">
				<view class="select-left">微信账号</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select"><input type="text" v-model="wechat"/></view>	 
				
			</view>
			<view class="item">
				<view class="select-left">QQ账号</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select"><input type="text" v-model="qq"/></view> 
				
			</view>
			
		</view>
		
		<view class="foot">
			<text>修改密码</text>
		</view>

	</view>
</template>

<script>
	import firsthead from '../../components/firsthead/firsthead.vue'
	export default {
		data() {
			return {
				phone:"13700000000",
				wechat:"未绑定",
				qq:"未绑定",
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

	.item{
		height: 80rpx;
		width: 640rpx;
		line-height: 80rpx;
		margin-left: 65rpx;
		float: left;
		
	}

	.passage{
		background-color: white;
		
		width: 100%;
		height: 270rpx;
		
		
	}
	
	.select-left{
		margin-top: 15rpx;
		float: left;
	}
	
	.iconfont{
		margin-top: 18rpx;
		margin-left: 15rpx;
		float: right;
	}
	.select{
		margin-top: 37rpx;
		width: 320rpx;
		float: right;	
		text-align: right;
	}

	.foot{
		background-color: white;
		margin-top: 30rpx;
		width: 100%;
		height: 95rpx;
		padding-left: 65rpx;
		line-height: 95rpx;
	}
	
	
	
	
	


</style>
