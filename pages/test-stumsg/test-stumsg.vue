<template>
	
	<view style="width: 750rpx; height: 1625rpx;background-color: #eee;">
		<firsthead title="学生信息"></firsthead>
		<view class="item" v-for="msg in msgs" :key="msg">
		
		<view>
			<image :src="msg.url" style="width: 100rpx; height: 100rpx; border-radius: 50%;margin-top:50rpx ;margin-left: 250rpx; "></image>
		</view>
		
		
		<view style="font-size: 35rpx;margin-top: 10rpx;text-align: center;">{{msg.name}}</view>
		<view style="width: 420rpx;margin-top: 60rpx;">
		<view class="wenzi">
			学校
			<text class="wenzi-right">{{msg.school}}</text>
		</view>
		<view class="wenzi">
			年级
			<text style="wenzi-right">{{msg.banji}}</text>
		</view>
		<view class="wenzi">
			联系方式
			<text style="wenzi-right">{{msg.phone}}</text>
		</view>
		</view>
		
		</view>
		
		<view style="float: left;margin-top: 100rpx;margin-left: 300rpx; width: 120rpx;height: 120rpx;background-color: #5276f0;font-size: 80rpx;text-align: center;color: white;border-radius: 50%;">+</view>
	</view>
</template>

<script>
	import firsthead from "@/components/firsthead/firsthead.vue";
	export default {
		
		data() {
			return {
				msgs:[
					{me:1, url:"../../static/image/头像.jpg", name:"宝贝小刘",school:"望子成龙小学",banji:"一年级",phone:"13000000000"},
					{me:2, url:"../../static/image/作业.png", name:"宝贝小黄",school:"望子成龙小学",banji:"一年级",phone:"13000000000"},
					
				]
			}
		},
		components:{firsthead},
		
		methods: {
			
		}
	}
</script>

<style>
	.item{
		float: left;
		width:600rpx;
		height: 500rpx;
		background-color: white;
		margin: 20rpx 75rpx 40rpx;
		border-radius: 40rpx;
		
	}
	.wenzi{
		
		margin-top: 20rpx;
		margin-left: 90rpx;
		height: 50rpx;
		width: 420rpx;
	}
	.wenzi text{
		float: right;
	}
</style>
