<template>
	<view class="first">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title=""></firsthead>
		</view>
		<view class="login">
		<view class="uni-form-item uni-column">
			<view class="login_big"></view>
			<view class="login_small">注册中</view>
		</view>
		<view class="middle">
		<view class="uni-form-item uni-column">
			<view>	
			<input class="uni-input" v-model="username" focus placeholder="请设置5-18位的新密码"/> 
			</view>
		</view>
		<view class="uni-form-item uni-column">
			<view>
			<input class="uni-input" v-model="password" focus placeholder="再次确认密码"/> 
			</view>
		</view>
		<view class="uni-form-item uni-column">
			<view>	
			<button type="primary" @click="user_login">登录</button>
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
		padding: 20rpx 78rpx;
		margin-top: 30rpx;
		text-align: center;
		
		
		.login_big{
			width: 94rpx;
			height: 94rpx;
			background-color: white;
			border-radius: 50%;
			margin-left: 245rpx;
			border: 8rpx #4678FA solid;
			
		}
		
		.login_small{
			font-family: "标题黑";
			font-size: 30rpx;
			margin-top: 35rpx;
			text-align: center;
			padding-bottom: 50rpx;
			
		}
		.middle{
			margin-top: 100rpx;
		}
		.uni-input{
			background-color: #fff;
			height: 80rpx;
			text-align: center;
			border-radius: 50rpx;
			padding-left: 10rpx;
			font-family: "标题黑";
			font-size: 30rpx;
		}
		
		.uni-form-item{
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
