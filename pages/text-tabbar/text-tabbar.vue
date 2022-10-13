<template>
	<view>
		<tab-bar ref="tabBar" :tabs="tabs" v-model="tabIndex"></tab-bar>
	    <view class="content">
			<view class="name">
				<text>小猪猪</text>
				<image src="../../static/image/正三角形.png"></image>
			</view>
			<view class="ketang">
				<view class="icon">
					<image src="../../static/image/作业.png"></image>
				</view>
				<text>考试</text>
			</view>
			<view class="ketang">
				<view class="icon">
					<image src="../../static/image/请假.png"></image>
				</view>
				<text>请假</text>
			</view>
			<view class="ketang">
				<view class="icon">
					<image src="../../static/image/operation.png"></image>
				</view>
				<text>作业</text>
			</view>
			<view class="ketang">
				<view class="icon">
					<image src="../../static/image/签到-copy.png"></image>
				</view>
				<text>签到</text>
			</view>
		</view>
	</view>
</template>

<script>
	import tabBar from '@/components/top-tabbar/top-tabbar.vue'
	export default {
		components: {
					tabBar
				},

		data() {
			return {
				tabs: [{name: '题库'}, {name: '课堂'}, {name: '智慧树'}],
			    tabIndex: 1, // 当前tab的下标

			}
		},
		methods: {


		}
	}
</script>

<style>
	.content{
		background-color: #eee;
		width: 750rpx;
		height: 1470rpx;
		
	}
	.name{
		height: 70rpx;
		width: 190rpx;
		background-color: white;
		border-radius: 50rpx;
		margin-left: 45rpx;
		float: left;
	}
	.name text{
		font-size: 25rpx;
		float: left;
		margin-top: 18rpx;
		margin-left: 25rpx;
		
	}
	.name image{
		width: 20rpx;
		height: 16rpx;
		float: right;
		margin-top: 28rpx;
		margin-right: 20rpx;
	}
	.ketang{
		background-color: white;
		width: 655rpx;
		height: 160rpx;
		margin-left: 45rpx;
		margin-top: 30rpx;
		float: left;
		border-radius: 40rpx;
	}
	.icon{
		width: 110rpx;
		height: 110rpx;
		background-color: #eeeeee;
		border-radius: 50%;
		float: left;
		margin:25rpx;
		
	}
	.icon image{
		width: 65rpx;
		height: 65rpx;
		float: left;
		margin: 24rpx;
	}
	.ketang text{
		font-size: 35rpx;
		float: left;
		line-height: 150rpx;
	}
</style>

