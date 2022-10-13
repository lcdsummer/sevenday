<template>
	<view class="first">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title=""></firsthead>
		</view>
		<view class="login">
		<view class="uni-form-item uni-column">
			<view class="login_big">登录</view>
			<view class="login_small">若该手机号未注册，我们将自动为您注册。</view>
		</view>
		<view class="middle">
		<view class="uni-form-item uni-column">
			<view  class="uni-input">	
			<input v-model="username" focus placeholder="请输入手机号"/> 
			</view>
		</view>
		
		<view class="uni-form-item">
			<view class="uni-input">
			<input v-model="smsAlert" focus placeholder="请输入短信验证码"/> 
			<view class="yzm">获取验证码</view>
			<view class="line"></view>
			</view>
		</view>
		<view class="uni-form-item uni-column">
			<view class="uni-form-button">	
			<button type="primary" @click="user_login">登录</button>
			</view>
		</view>
		<view class="middle-footer">
			<view class="middle-footer-left">	
			<text>密码登录</text>
			</view>
			
		</view>
		</view>
		<view class="foot">
			<view class="foot_text">登录或注册即代表同意并阅读<text>《用户协议》</text>及<text>《隐私协议》</text></view>
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
			
		}
	}
</script>

<style lang="scss">
	.first{
		width: 750rpx;
		height: 1625rpx;
		background-color: #eee;
		
	.login{
		padding: 20rpx 78rpx;
		margin-top: 30rpx;
		text-align: center;
		
		
		.login_big{
			font-family: "标题黑";
			font-weight: bold;
			font-size: 50rpx;
			text-align: left;
			
		}
		
		.login_small{
			font-family: "标题黑";
			font-size: 20rpx;
			margin-top: 35rpx;
			text-align: left;
			
		}
		.middle{
			margin-top: 100rpx;
		}
		.uni-input{
			width: 600rpx;
			background-color: #fff;
			border-radius: 50rpx;
		}
		.yzm{
			position: absolute;
			z-index: 100;
			left: 490rpx;
			top:590rpx;
			font-size: 30rpx;
			color: #4678FA;
			
		}
		.line{
			position: absolute;
			z-index: 100;
			left: 460rpx;
			top:590rpx;
			width: 1rpx;
			height: 43rpx;
			background-color: #eaeaea;;
		}
		.uni-form-item input{
			text-align: left;
			font-family: "标题黑";
			font-size: 30rpx;
			padding-left: 10rpx;
			height: 80rpx;
			width: 400rpx;
			
		}
		
		.uni-form-item{
			margin: 35rpx 0;
		}
		.uni-form-button{
			margin: 40rpx 0;
		}
		button{
			border-radius: 50rpx;
			font-family: "标题黑";
			font-size: 30rpx;
		}
		.middle-footer{
			margin-top: 50rpx;
		}
		
		
		.middle-footer-left{
			font-size: 25rpx;
			font-family: "标题黑";
			float: left;
		}
	}
	.foot{
		margin-top: 700rpx;
		font-family: "标题黑";
		font-size: 20rpx;
	}
	.foot_text text{ 
		color: #4678FA;
		 }
	}
</style>
