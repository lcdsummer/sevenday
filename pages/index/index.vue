<template>
	<view>
		<view class="content">
			<scroll-view class="noScorll bar-view" scroll-x scroll-with-animation>
				<view class="titleBar">

					<view class="barItem" v-for="(item,index) in tabs" :key="index" @click="changeTab(index)">
						<view :class="{'textBar':index==value,'textBar2':index!=value}">{{item.name}}</view>
						<view :class="{'bottomLine':index==value,'bottomLine2':index!=value}"></view>
					</view>

				</view>
			</scroll-view>
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
		background-color: #FFFFFF;
		padding: 20rpx;
		border-bottom: 1px solid #C0C0C0;
	}

	.bar-view {
		width: 100%;
		text-align: center;
		white-space: nowrap;

	}

	.titleBar {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.barItem {
		display: flex;
		flex-direction: column;
		margin-right: 40rpx;
	}

	.bottomLine {
		width: 70rpx;
		height: 10rpx;
		background-color: #FFAC3E;
		border-radius: 10rpx;
		margin-top: 10rpx;
	}

	.bottomLine2 {
		width: 70rpx;
		height: 10rpx;
		border-radius: 10rpx;
		margin-top: 10rpx;
	}

	.textBar {
		color: #FFAC3E;
	}

	.textBar2 {
		color: #160e05;
	}

	.line {
		height: 1px;
		background-color: #CCCCCC;
		margin: 20rpx 20rpx;
	}
</style>

