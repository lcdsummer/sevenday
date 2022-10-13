<template>
	<view class="first">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title=""></firsthead>
		</view>
		<view class="login">
		<view class="uni-form-item uni-column">
			<view class="login_big">登录</view>
			<view class="login_small">欢迎进入少年代码。</view>
		</view>
		<view class="middle">
		<view class="uni-form-item uni-column">
			<view>	
			<input class="uni-input" v-model="username" focus placeholder="请输入手机号"/> 
			</view>
		</view>
		<view class="uni-form-item uni-column">
			<view>
			<input class="uni-input" v-model="password" focus placeholder="请输入密码"/> 
			</view>
		</view>
		<view class="uni-form-item uni-column">
			<view>	
			<button type="primary" @click="user_login">登录</button>
			</view>
		</view>
		<view class="middle-footer">
			<view class="middle-footer-left">	
			<text>验证码登录</text>
			</view>
			<view class="middle-footer-right">
			<text>忘记密码</text>
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
			background-color: #fff;
			height: 80rpx;
			text-align: left;
			border-radius: 50rpx;
			padding-left: 10rpx;
			font-family: "标题黑";
			font-size: 30rpx;
		}
		
		.uni-form-item{
			margin: 30rpx 0;
		}
		.search-span{
			width: 40rpx;
			height: 40rpx;
			margin-top: 12rpx;
			margin-left: 20rpx;
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
			font-size: 20rpx;
			font-family: "标题黑";
			float: left;
		}
		
		.middle-footer-right{
			font-size: 20rpx;
			font-family: "标题黑";
			float: right;
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
