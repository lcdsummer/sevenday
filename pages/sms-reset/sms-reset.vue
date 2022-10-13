<template>
	<view class="first">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title=""></firsthead>
		</view>
		<view class="login">
		<view class="uni-form-item">
			<view class="login_big">短信重置</view>
			<view class="login_small">密码长度在5-18位，应包含数字、大小字母、特殊字符（除空格）的两种或两种以上</view>
		</view>
		<view class="middle">
		<view class="uni-form-item">
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
		<view class="uni-form-item">
			<view class="uni-input">
			<input v-model="newPassword" focus placeholder="请输入新密码密码"/> 
			</view>
		</view>
		<view class="uni-form-item">
			<view class="uni-input">
			<input v-model="passwordNew" focus placeholder="请重复输入新密码"/> 
			</view>
		</view> 
		<view>
			<button type="primary" @click="user_login">确定</button>
		</view>
		<view class="middle-footer">
			<view class="middle-footer-right">
			<text>邮箱重置</text>
			</view>
		</view>
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
		padding: 20rpx 75rpx;
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
			font-size: 21rpx;
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
		.uni-form-item input{
			text-align: left;
			font-family: "标题黑";
			font-size: 30rpx;
			padding-left: 10rpx;
			height: 80rpx;
			width: 400rpx;
			
		}
		
		.yzm{
			position: absolute;
			z-index: 100;
			left: 490rpx;
			top:605rpx;
			font-size: 30rpx;
			color: #4678FA;
			
		}
		.line{
			position: absolute;
			z-index: 100;
			left: 460rpx;
			top:605rpx;
			width: 1rpx;
			height: 43rpx;
			background-color: #eaeaea;;
		}
		.uni-form-item{
			margin: 30rpx 0;
			
		}
		.uni-form-button{
			margin: 50rpx 0;
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
	}
</style>
