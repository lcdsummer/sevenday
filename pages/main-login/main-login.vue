<template>
	<view class="login">
			
		<view class="login_head">
			<view class="eye-left"></view>
			<view class="eye-right"></view>
		</view>
		
		<view class="login_middle">	
		
		<view class="uni-form-item">
			<view>	
			<button type="primary" @click="user_login">
				<view>
				<image class="weixin-span" src="../../static/image/weixin.png"/>
				</view>
				<text>微信登录</text>
				
			</button>
			</view>
		</view>
		
		<view class="uni-form-item">
			<view>	
			<button type="primary" @click="user_login" >手机号登录</button>
			</view>
		</view>
		
		</view>
		
		<view class="middle-footer">
			<view class="middle-footer-center">
			<view class="line"></view>
			<text space="emsp" decode="true">{{''}}&emsp;其他方式登录{{' '}}&emsp;</text>
			<view class="line"></view>
			</view>
		</view>
		
		<view class="qq">
			<image class="qq-span" src="../../static/image/qq.png"/>
		</view>
		
		
		<view class="foot">
			<checkbox :checked="agree_check"  @click="moutcl" />
			<view class="foot_text">登录即代表同意并阅读《用户协议》及《隐私协议》</view>
		</view>


	</view>
</template>

<script>
	export default {
		data() {
			return {
				gouxSta:false,
			}
		},
		components : {
			
		},
		methods: {
			moutcl(){
					if( this.gouxSta == false){
						this.gouxSta = true
					}else{
						this.gouxSta = false
					}
				},
				
			user_login(){
				if( this.gouxSta == false){
					uni.showToast({
						"title":"请勾选用户协议和隐私协议",
						"icon":'none'
					})		
				}else{
							
				}		
			},
		}
	}
</script>

<style scoped>
	.login{
		width: 750rpx;
		height: 1625rpx;
		background-color: #4678FA;
	}
	.login_head{
		width: 100%;
		height: 230rpx;
		padding-top: 295rpx;
	}
	.eye-left{
		float: left;
		margin-left: 192rpx;
		width: 85rpx;
		height: 100%;
		background-color: white;
		border-radius: 50rpx;
	}
	.eye-right{
		float: right;
		margin-right: 192rpx;
		width: 100rpx;
		height: 100%;
		background-color: white;
		border-radius: 50rpx;
	}
		
		
	.login_middle{
		margin-top: 300rpx;
	}

	.uni-form-item{
		margin: 30rpx 0;
	}
	.weixin-span{
		margin-top: 18rpx;
		margin-left: 170rpx;
		float: left;
		width: 40rpx;
		height: 40rpx;
	}
	button text{
		float: left;
		margin-left: 10rpx;
	}
	button{
		width: 570rpx;	
		background-color: white;
		color: #4678FA;
		border-radius: 50rpx;
		font-family: "标题黑";
		font-size: 30rpx;
		text-align: center;
			
	}
	.middle-footer{
		margin-top: 100rpx;
		margin-left: 190rpx;
	}
	.middle-footer-center text{
			
		float: left;
		font-size: 25rpx;
		text-align: center;
		color: white;
			
	}
	.line{
		float: left;
		height:3rpx;
		width: 80rpx;
		background-color: white;
		margin-top: 18rpx;
	}
	
	.qq{
		width: 100%;
		margin-top: 190rpx;
	}
	.qq-span{
		margin-left: 320rpx;
		width: 90rpx;
		height: 90rpx;
	}
	.foot{
		width: 100%;
		
		margin-top: 50rpx;
	}
	.foot_text{
		float: right;
		margin-right: 150rpx;
		margin-top: 5rpx;
		font-size: 20rpx;
		color: white;
	}
	
	/* checkbox样式 */
	>>> uni-checkbox .uni-checkbox-input{
		float: left;
		margin-left: 110rpx;
		width: 20rpx;
		height: 20rpx;
		border-radius: 50% ;
		background-color: white !important;
	}
	
	/* 选中时的样式 */
	>>> uni-checkbox .uni-checkbox-input.uni-checkbox-input-checked{
		background-color: white !important;
		color: #4678FA !important; 
	}
	

	

	

</style>
