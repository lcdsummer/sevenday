<template>
	<view class="four">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title="协议名"></firsthead>
		</view>
		<view class="passage">
		<view class="wenzi">
		<text space="emsp" decode="true">{{' '}}&emsp;坚持党的全面领导，最根本的就是坚决维护党中央权威和集中统一领导，不断增强“四个意识”、坚定“四个自信”、做到“两个维护”</text>
        </view>
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
	
	.four{
		width: 750rpx;
		height: 1625rpx;
		background-color: #eee;
		.passage{
			background-color: white;
			height: 1410rpx;
			width: 690rpx;
			border-radius: 28rpx;
			margin-left: 30rpx;
			margin-bottom: 65rpx;
		}
		.passage::before{
			content: '';
			display: table;
		}/*解决外边距重叠*/
		.wenzi{
			float: left;
			margin-top: 35rpx;
			margin-left: 35rpx;
			margin-right: 35rpx;
			font-size: 30rpx;
		}

		
	}
</style>
