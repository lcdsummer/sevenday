<template>
	<view>
		<view class="content">
			<view class="bar-view">
				<view class="titleBar">

					<view class="barItem" v-for="(item,index) in tabs" :key="index" @click="changeTab(index)">
						<view :class="{'textBar':index==value,'textBar2':index!=value}">{{item.name}}</view>
						<view :class="{'bottomLine':index==value,'bottomLine2':index!=value}"></view>
					</view>

				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			value: { // vue 语法糖, v-model双向绑定：1. props声明value, 2. 修改它时触发input事件传递
				type: Number,
				default: 0
			},
			tabs: { // 标签选项数组
				type: Array,
				default: () => [{
						id: 1,
						name: '1'
					},
					{
						id: 2,
						name: '2'
					},
					{
						id: 3,
						name: '3'
					}
				]
			}
		},

		data() {
			return {

			}
		},
		methods: {

			//  切换标签选项
			changeTab(index) {
				this.$emit('input', index)
			}

		}
	}
</script>

<style>
	.content {
		width: 750rpx;
		height: 155rpx;
		background-color: #eeeeee;		
	}

	.bar-view {
		width: 100%;
		height: 155rpx;
		text-align: center;
		white-space: nowrap;

	}

	.titleBar {
		display: flex;
		flex-direction: row;
		align-items: center;
		padding-left: 110rpx;
		padding-top: 77rpx;
	}

	.barItem {
		display: flex;
		flex-direction: column;
		margin-left: 70rpx;
		font-size: 30rpx;
	}

	.bottomLine {
		width: 77rpx;
		height: 10rpx;
		background-color: #4778fa;
		border-radius: 10rpx;
		margin-top: 30rpx;
		position: absolute;
	}

	.bottomLine2 {
		width: 77rpx;
		height: 10rpx;
		border-radius: 10rpx;
		margin-top: 0rpx;
		position: absolute;
	}

	.textBar {
		z-index: 100;
		color: black;
		font-weight: bold;
		margin-left: 8rpx;
	}

	.textBar2 {
		z-index: 100;
		color: #989898;
		margin-left: 8rpx;
	}

	
</style>

