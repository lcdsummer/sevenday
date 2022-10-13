<template name="StuMsg">
	
	<view style="width: 750rpx; background-color: #eee;">
		<!--float: left;  -->
		<TalkHead title="学生信息"></TalkHead>
		<view style="float: left; width: 750rpx;height: 120rpx;background-color: #eee;"></view>
		<br>
		<view v-for="msg in msgs" :key="msg">
			<view v-if="msg.me === true">
				<view style="float: left; width:600rpx;height: 500rpx;background-color: aqua;">
					<!--float:right;position: relative;right: 0rpx;  right: 3%; background-color: white;-->
					<text style="font-size: 30rpx;">{{msg.name}}</text>
					<view style="height: 160;width: 420rpx;">
						<!-- float:right;position: relative; right: 3%; -->
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
		</view>
		</view>	
	</view>
</template>

<script>
	import TalkHead from '@/components/talk-head/talk-head.vue'
	export default {
		components: {TalkHead},
		name:"StuMsg",
		
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
			msgs: {//聊天列表
				type: Array,
			    value: []
			},
		},
		data:{
			
		},
		methods:{
			
		}
	}
</script>

<style>
	.wenzi{
		height: 50rpx; 
		width: 420rpx;
		color: antiquewhite;
	}
	
</style>