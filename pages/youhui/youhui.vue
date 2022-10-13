<template>
	<view class="third">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title="我的优惠券"></firsthead>
		</view>
		<view class="white">
		<view class="blue">
		<view class="answer-card">
			<image class="search-span" src="../../static/image/优惠券.png"/>
		</view>
		</view>
		</view>
		<view class="text">
			<text>
			暂时没有优惠券
			</text>
		</view>
	</view>	
</template>

<script>
	import firsthead from '../../components/firsthead/firsthead.vue'
	export default {
		data() {
			return {
				
			}
		},
		components : {
			firsthead
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	
	.third{
		width: 750rpx;
		height: 1625rpx;
		background-color: #eee;
		.white{
			height: 155rpx;
			width: 200rpx;
			background-color: white;
			border-radius: 70rpx;
			margin-top: 550rpx;
			margin-left: 280rpx;
			float: left;
		}
		.blue{
			float: left;
			width: 145rpx;
			height: 125rpx;
			background-color: #d9e7f4;
			border-radius: 50%;
			margin-top: 17rpx;
			margin-left: 30rpx;
		}
		.search-span{
			float: left;
			width: 75rpx;
			height: 70rpx;
			margin-top: 27rpx;
			margin-left: 34rpx;
		}

		.text text{
			float: left;
			color: #727272;
			margin-top: 20rpx;
			margin-left: 290rpx;
		}
	}
</style>
