<template>
	
	<view style="width: 750rpx; height: 2000rpx;">
	<!--	<firsthead title="试卷"></firsthead>-->
		
		
		<!--倒计时-->
		<countdown-timer ref="countdown" :time="time" @finish="onFinish" autoStart >
			<template v-slot="{day, hour, minute, second, remain, time}">
				
				<!-- 自定义样式 -->
				<view class="case">
					<view class="title">剩余时间</view>
					<view class="custom">
						
						<!-- #ifndef MP -->
						<view>{{fillWithZero(minute, 2)}}</view>
						<view>:</view>
						<view>{{fillWithZero(second, 2)}}</view>
						<!-- #endif -->
						
						<!-- #ifdef MP -->
						<!-- 小程序暂时不支持在v-slot内部调用方法，后期可能会支持 -->
						<view>{{minute}}</view>
						<view>:</view>
						<view>{{second}}</view>
						<!-- #endif -->
						
					</view>
				</view>
				
				</template>
			
		</countdown-timer>
		<!--倒计时-->

		<!--
		<view v-for="msg in msgs" :key="msg">	
		<view class="item"  v-if="msg.me===1">
			
		<view style="color: blue; margin: 30rpx;">{{msg.tnum}}<text style="color: black;">/10</text>选择题</view>
		
		<view>{{msg.timu}}</view>
		
		<view>
			<image :src="msg.url" style="width: 100rpx; height: 100rpx; border-radius: 50%;margin-top:50rpx ;margin-left: 250rpx; "></image>
		</view>
		
		<view style="width: 420rpx;margin-top: 60rpx;">
		<view v-for="xuanz in msg.xuanzs" :key="xuanz">
		<view class="xuanz">
			<view class="zimu"></view>
			<view v-for="item in xuanz.A" :key="item">{{item}}</view>
		</view>
		</view>
		</view>
		
		</view>
		</view>
		-->
	</view>
</template>

<script>
	import firsthead from "@/components/firsthead/firsthead.vue";
	
	export default {
		
		data() {
			return {
				time: new Date('2020/04/24 01:00:00').getTime() - new Date('2020/04/24 00:50:00').getTime(),
				flag:-1,
				msgs:[
					{
						me:1, 
						tnum:"01",
						timu:"1.以下程序执行后，角色面向的方向是？（）【多角色设置】",
						url:"../../static/image/头像.jpg",
						xuanzs:[
							{
								A:["A","右上"],
								B:["A","右下"],
								C:["A","左上"],
								D:["A","坐下"],
							}
						 ]
						
						},
					{
						me:2, 
						tnum:"02",
						timu:"2.以下程序执行后，角色面向的方向是？（）【多角色设置】",
						url:"../../static/image/头像.jpg",
						xuanzs:[
							{
								zimus:["A","B","C","D"],
								zimuys:["右上","右下","左上","左下"]
							}
						]
						},
					]
			}
		},
		components:{firsthead},
		
		methods: {
			choseprofrom:function (index) {
				this.flag = index;
			},
			onFinish() {
					uni.showToast({
						icon: 'none',
						title: '考试时间已结束'
					})
				},
				fillWithZero(num, n) {
					var len = num.toString().length;
					while (len < n) {
						num = "0" + num;
						len++;
					}
					return num;
				}
			}

		
	}
</script>

<style>
	.selected {
		color: white;
		background-color: red;
	}
	.item{
		float: left;
		width:660rpx;
		height: 960rpx;
		background-color: white;
		margin: 110rpx 55rpx 40rpx;
		border-radius: 40rpx;
		
	}
	
	.zimu{
		text-align: center; 
		float: left; 
		width: 60rpx; 
		height: 60rpx;
		border-radius: 50%;
		background-color: #eee;
	}
	.xuanz{
		margin-top: 30rpx;
		margin-left: 80rpx;
		line-height: 65rpx;
		width: 300rpx;
		height: 70rpx;
		border-radius: 50rpx;
		background-color: bisque;
	} 
	/*倒计时 */
	.container {
		padding: 20upx;
	}
	.case {
		display: flex;
		margin: 20upx;
	}
	.title {
		margin-right: 10upx;
		color: #7f7f7f;
	}
	.custom {
		display: flex;
		color: #7f7f7f;
	}
	/*倒计时 */
</style>
