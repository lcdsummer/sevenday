<template>
	<view class="second">
	<view class="search-head">
	<view class="phone-search">
		<image class="search-span" src="../../static/image/searchSpan.png"/>
		<input type="text" placeholder="请输入您要查找的手机号" placeholder-style="color:#dadada"/>
	</view>
	<text class="quxiao">取消</text>
	</view>
	
	<!--弹窗-->
	<view @tap="tapPopup" style="float: left;margin: 250rpx 300rpx;background-color: aqua">我是弹窗</view>
	
	<view class="popup" v-show="show">
			<view class="popup-info">
				<view style="height: 610rpx;width: 410rpx;margin: 100rpx 95rpx;">
					
					<view >
					<image src="../../static/image/头像.jpg" mode='aspectFill' style="float: left; margin-top:70rpx;margin-left: 130rpx;width: 160rpx; height: 160rpx;border-radius: 50%;"></image>
				    </view>
					
					<view style="float: left;width: 410rpx;height: 70rpx;border-bottom: 3rpx #eee solid; margin-top:20rpx;text-align: center; font-size: 32rpx; font-weight: bold;">宝贝猪</view>
					
					<view style="border-bottom: 3rpx #eee solid; float: left; width: 410rpx;height: 340rpx;">
						<view class="item">
							年龄
							<text>9岁</text>
						</view>
						<view class="item">
							地区
							<text>广东省深圳市</text>
						</view>
						<view class="item">
							简介
							<text>
								这个人很懒，什么都没写<br/>
								这个人很懒，什么都没写<br/>
								这个人很懒，什么都没写
							</text>
						</view>
					</view>
					
					</view>
					<view class="popup-btn">
					<view type="default" @tap="cancel" style="margin-left: 210rpx; background-color: #5276f0;height: 75rpx;width: 170rpx;border-radius: 50rpx; color: white;text-align: center;line-height: 70rpx;font-size: 50rpx;">+</view>
					<view type="default" class="affirm" @tap="affirm" style="height: 110rpx;float: left;margin-left: 270rpx;  font-size: 25rpx;line-height: 110rpx;color: #6f6f6f;" >取消</view>
					</view>
			</view>
			</view>
	</view>
	<!--弹窗-->
	
	</view>
</template>						

<script>
	export default {
		data() {
			return {
				show:false,
			}
		},
		methods: {
			// 弹窗
					tapPopup() {
						this.show = true;
					},
					// 点击弹窗取消
					cancel() {
						this.show = false;
					},
					// 点击弹窗确认
					affirm() { 
						this.show = false;
					}

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
	
	/*弹窗*/
	.popup {
		position: absolute;
		left: 0;
		right: 0;
		top: 0;
		height: 1625rpx;
		width: 750rpx;
		background-color: rgba(0,0,0,0.6);
		z-index: 9998;
	}

	.popup-info{
		position: absolute;
		width: 590rpx;
		height: 990rpx;
		top: 50%; 
		left: 50%;
		transform: translate(-50%, -50%);
		font-size: 30upx;
		border-radius: 20upx;
		background-color: #fff;
		z-index: 9999;
	}
	.item{
		font-size: 32rpx;
		width: 100%;
		margin-top: 20rpx;
		margin-bottom: 20rpx;
		float: left;
		
	}
	.item text{
		float: right;
		font-size: 24rpx;
		color: #6f6f6f;
	}
	/*弹窗*/

</style>
