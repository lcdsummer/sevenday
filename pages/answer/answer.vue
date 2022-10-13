<template>
	<view class="third">
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title="答题卡"></firsthead>
		</view>
		<view class="answer-card">
			<view class="danxuan">
				<text>单选题</text>
				<view class="answer-status"><view class="wenzi">1</view></view>
				<view class="answer-status"><view class="wenzi">2</view></view>
				<view class="answer-status"><view class="wenzi">3</view></view>
				<view class="answer-status"><view class="wenzi">4</view></view>
				<view class="answer-status"><view class="wenzi">5</view></view>
				<view class="answer-status"><view class="wenzi">6</view></view>
				<view class="answer-status"><view class="wenzi">7</view></view>
				<view class="answer-status"><view class="wenzi">8</view></view>
				<view class="answer-status"><view class="wenzi">9</view></view>
				<view class="answer-status"><view class="shuang-wenzi">10</view></view>
			</view>
			<view class="duoxuan">
				<text>多选题</text>
				<view class="answer-status"><view class="shuang-wenzi">11</view></view>
				<view class="answer-status"><view class="shuang-wenzi">12</view></view>
				<view class="answer-status"><view class="shuang-wenzi">13</view></view>
				<view class="answer-status"><view class="shuang-wenzi">14</view></view>
				<view class="answer-status weixuan"><view class="weixuan-wenzi">15</view></view>
				<view class="answer-status weixuan"><view class="weixuan-wenzi">16</view></view>
				<view class="answer-status weixuan"><view class="weixuan-wenzi">17</view></view>
				<view class="answer-status weixuan"><view class="weixuan-wenzi">18</view></view>
				<view class="answer-status weixuan"><view class="weixuan-wenzi">19</view></view>
				<view class="answer-status weixuan"><view class="weixuan-wenzi">20</view></view>
			</view>
		</view>
		<view class="answer-button">
			<text class="answer-button-color">交卷</text>
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
		
		.answer-card{
			height: 640rpx;
			width: 650rpx;
			background-color: white;
			border-radius: 50rpx;
			margin-left: 50rpx;
			margin-top: 25rpx;
			
		}
		.answer-card::before{
			content: '';
			display: table;
		}/*解决外边距重叠*/
		
		.danxuan{
				width: 595rpx;
				height: 230rpx;
				background-color: white;
				margin-top: 50rpx;
				margin-left: 30rpx;
			}
		
		.danxuan text{
			color: #4678FA;
			margin-left: 20rpx;
		}
		.danxuan text::after{
		    content: '';
		    display: table;
		    clear: both;
		}
		.answer-status{
			width: 60rpx;
			height: 60rpx;
			border-radius: 50%;
			background-color: #4678FA;
			float: left;
			margin: 20rpx;

			.wenzi{
				margin-top: 15rpx;
				margin-left: 22rpx;
				color: white;
				font-size: 25rpx;
			}
			.shuang-wenzi{
				margin-top: 15rpx;
				margin-left: 18rpx;
				color: white;
				font-size: 25rpx;
			}
		}
		.duoxuan{
				width: 595rpx;
				height: 230rpx;
				background-color: white;
				margin-top: 50rpx;
				margin-left: 30rpx;
			}
		
		.duoxuan text{
			color: #4678FA;
			margin-left: 20rpx;
		}
		.duoxuan text::after{
		    content: '';
		    display: table;
		    clear: both;
		}
		.answer-status{
			width: 60rpx;
			height: 60rpx;
			border-radius: 50%;
			background-color: #4678FA;
			float: left;
			margin: 20rpx;
			.shuang-wenzi{
				margin-top: 15rpx;
				margin-left: 18rpx;
				color: white;
				font-size: 25rpx;
			}
		}
		.weixuan{
			width: 60rpx;
			height: 60rpx;
			border-radius: 50%;
			background-color: #EEEEEE;
			float: left;
			margin: 20rpx;
		}
		.weixuan-wenzi{
			margin-top: 15rpx;
			margin-left: 18rpx;
			color: black;
			font-size: 25rpx;
		}
		.answer-button{
			width: 650rpx;
			height: 97rpx;
			border-radius: 50rpx;
			margin-left: 50rpx;
			background-color: #E1F0FF;
			margin-top: 95rpx;
		}
		.answer-button::after{
		    content: '';
		    display: table;
		    clear: both;
		}
		.answer-button-color{
			float: left;
			margin-top: 28rpx;
			margin-left: 300rpx;
			color: #4678FA;
			font-size: 30rpx;
		}

		
	}
</style>
