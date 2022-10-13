<template>
	<view class="tab-bar">
		<view v-for="(item,index) in list" :key="index" :class="select === index? 'select' : 'tab-bar-item'"  @click="switchTab(item, index)">
			<view class="tab_text">{{item.text}}</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:['select'],
		data() {
			return {
				activeclass: 0,
				color: "#333333",
				selectedColor: "#333333",
				list: [{
					text: "课堂"
				}, {
					text: "学习"
				}, {
					text: "私信"
				}, {
					text: "我的"
				}],
				switchPages:['../../pages/home/login','../../pages/healthy/study','../../pages/information/information','../../pages/my/my']
			}
		},
		methods: {
			switchTab(item, index) {
				uni.switchTab({
					url: this.switchPages[index]
				})
			}
		}
	}
</script>

<style lang="less" scoped>
	.tab-bar {
		position: absolute;
		
		top: 1500rpx;
		height: 120rpx;
		width: 100%;
		background: white;
		/*display: flex;*/
		justify-content: center;
		align-items: center;
		padding-bottom: env(safe-area-inset-bottom); 
		.select {
			height: 70rpx;
			width: 70rpx;
			text-align: center;
			justify-content: center;
			
			align-items: center;
			
			background-color: #4678FA;
			.tab_img {
				width: 37rpx;
				height: 41rpx;
			}
			.tab_text {
				position: absolute;
				float: left;
				z-index: 100;
				
				width: 100rpx;
				height: 100rpx;
				font-size: 28rpx;
				margin-top: 9rpx;
			}
		}
		.tab-bar-item {
			height: 100%;
			text-align: center;
			justify-content: center;
			align-items: center;
			.tab_img {
				width: 37rpx;
				height: 41rpx;
			}
			.tab_text {
				font-size: 28rpx;
				margin-top: 9rpx;
			}
		}
	}
</style>

