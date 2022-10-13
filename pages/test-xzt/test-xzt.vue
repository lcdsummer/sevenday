<template>
	<view class="content">
	<view class="header">
		<!--<text class="iconfont icon-fanhuijiantou"></text>-->
		<firsthead title="作业"></firsthead>
	</view>
	<view class="card">
		<view class="card-head">
			<view   v-for="(item,index) in topic" :key="index" class="tihao">
				<view class="topic-box">
				    <view>{{item.title}}/10<text>选择题</text></view>
				</view>
			</view>
			<view class="shuqian">答题卡</view>
		</view>
		
	</view>
	
	</view>
</template>

<script>
	
	export default{
		data() {
			return {
				topic: [ // 题目
				    { title: '01' },
				    { title: '02' },
				    { title: '03' },
				    { title: '04' },
				    { title: '05' },
				    { title: '06' },
				    { title: '07' },
				    { title: '08' },
				    { title: '09' },
				    { title: '10' }
				]

			}
		},
		components : {
			firsthead
		},
		onLoad() {
			
		},
		methods: {
			
		}
	}
</script>

<style scoped>
	.content{
		background-color: #eee;
		height: 1640rpx;
		width: 750rpx;
	}
	.card{
		background-color: white;
		width: 500rpx;
		height: 900rpx;
		border-radius: 40rpx;
	}
	.card-head{
		width: 100%;
		height: 100rpx;
	}
	.shuqian{
		width: 100rpx;
		height: 50rpx;
		background-color: aqua;
		color: blue;
		border-bottom-left-radius:50rpx;
		border-top-left-radius:50rpx;
	}
	.card{
		width: 500rpx;
		height: 500rpx;
	}
</style>
