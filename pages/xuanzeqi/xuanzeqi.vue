<template>
	<view class="five">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title="账号安全"></firsthead>
		</view>
		<view>
			<view class="item">
				<view class="left">手机号</view>
				<view><picker mode="selector" @change="bindPickerChange" :range="array" range-key="phone">{{array[index].phone}}</picker></view>
			</view>
			<view></view>
			<view></view>
		</view>
	</view>
</template>

<script>
	import firsthead from '../../components/firsthead/firsthead.vue'
	export default {
		data() {
			return {
				array:[{phone:'13398788231'},{phone:'10086'}],
				index:0
			}
		},
		components : {
			firsthead
		},
		methods: {
			bindPickerChange(e){
				this.index=e.detail.value
			}
		}
	}
</script>

<style lang="scss">
	
	.four{
		width: 750rpx;
		height: 1625rpx;
		background-color: #eee;
		
		.item{
			height: 80rpx;
			line-height: 80rpx;
			display: flex;
			border-bottom: solid 1rpx #123456;
		}
		
		.left{
			width:180rpx
		}
		
	}
</style>
