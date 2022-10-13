<template name="chat-text-list">
	
	<view class="width" style="float: left; width: 750rpx; background-color: #eee;">
		<TalkHead title="ZHANG SAN"></TalkHead>
		<view style="float: left; width: 750rpx;height: 120rpx;background-color: #eee;"></view>
		<br>
		<block v-for="msg in msgs" :key="msg">
			<block v-if="msg.me === true">
				<!--
				<view style="position: relative; width: 100%;">
					<text style="color: #CACACA;float: right;">{{my_name}}</text>
				</view>
				<br>
				-->
				<view style="float:right;position: relative;right: 0rpx;width: 80%;right: 3%;">
					
					<view style="margin: 40rpx 0rpx; float:right;position: relative; right: 3%;">
						<!--<view class="Separation-line">
							<view style="background-color: antiquewhite;float:right;position: relative; right: 0rpx; width: 10%;">
								<view style="float:right;position: relative;right: 0rpx;">
									<image style="width: 80rpx;height: 80rpx;" v-bind:src="my_image" mode=""></image>
								</view>
							</view>
						</view>-->
						<view class="" style=" padding: 18rpx 28rpx;text-align: right;background-color: white;border: 2rpx solid white;border-radius: 33rpx;">
							<view style="text-align: left;">
								<text style="font-size: 32rpx;color: black;word-break:break-all;">{{msg.msg}}</text>
							</view>
						</view>
					</view>
		
				</view>
			</block>
			<!-- --------------------------------------------------------------- -->
			<block v-if="msg.me === false">
				<view style="float: left; position: relative;width: 95%;">
					
					<view class="">
					<view style="margin-top: 30rpx; float: left;position: relative; left: 40rpx;">
						<view style="float: left;position: relative;">
							<image style="width: 80rpx;height: 80rpx; border-radius: 50%;" v-bind:src="my_image" mode=""></image>
						</view>
					</view>
					</view>
					<view style="margin: 40rpx 0rpx; float:left; position: relative; left: 10%;width: 72%;">
						
						<view class="" style="float: left;position: relative; padding: 18rpx 28rpx;text-align: left; background-color: #4678fa;border: 2rpx solid #4678fa;border-radius: 33rpx;">
							<view style="text-align: left;">
								<text style="font-size: 32rpx;color: white;word-break:break-all;">{{msg.msg}}</text>
							</view>
						</view>
					</view>
					
				</view>
			</block>
			<br>
			<br>
			<br>
		</block>
		<br>
		<br>
		<br>
		<br>
		<br>
		<view style="float: left; width: 100%; height: 200rpx;background-color: #eee;"></view>
		
		<view style="background-color:#eee;border-top: #e2e2e2 2rpx solid; width: 750rpx; height: 125rpx;position: fixed;bottom:0%;">
			<textarea v-model="input" style="float: left;border-radius: 50rpx;width: 680rpx; height: 67rpx;margin-left: 20rpx;margin-top: 25rpx; font-size: 40rpx;padding-top: 13rpx; padding-left: 30rpx; color: #000000; background-color: white;"></textarea>
			<button @tap="ev()" type="default" style="float: left; position: fixed; bottom: 28rpx; left: 650rpx; width: 65rpx;height: 65rpx;background-color: #009dff;border-radius: 50%;">
				
				<image style="float: left;width: 60rpx;position: relative;height: 60rpx;float: right; position: fixed; bottom: 30rpx; left: 650rpx;" src="../../static/image/发送.png"></image>
				<!--<uni-icons type="paperplane" size="25" color="white"></uni-icons>
-->
			</button>
		
		</view>
	</view>
</template>

<script>
	import uniIcons from "../chat-list/uni-icons.vue";
	import TalkHead from '@/components/talk-head/talk-head.vue'
	export default {
		components: {uniIcons,TalkHead},
		name:"ChatTextList",
		
		//属性
		props: {
			my_image: {//我的图片的路径
				type: String,
				value: null
			},
			other_image: {//对方的图片
				type: String,
				value: null
			},
			my_name:{
				type:String
			},
			other_name:{
				type:String
			},
			msgs: {//聊天列表
				type: Array,
				/* 
				使用方法：[{me:true, msg:"我发送的信息"}, {me:false, msg:"对方发送的信息"}]
				*/
			   value: []
			},
		},
		data:{
			input:"",
		},
		methods:{
			ev(){
				var get = this.input
				this.$emit("send",get)//传递的值
			}
		}
	}
</script>

<style>
	
</style>