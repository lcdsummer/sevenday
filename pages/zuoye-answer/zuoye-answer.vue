<template>
	<view class="content">
	<view class="header">
		<!--<text class="iconfont icon-fanhuijiantou"></text>-->
		<firsthead title="作业"></firsthead>
	</view>
	<view class="card">
		<view class="card-head">
			<view class="tihao">
				
			</view>
			<view class="shuqian">答题卡</view>
		</view>
		
		<view class="picker_group">
		          <text class='text'>备注</text>
		          <radio-group class="group" bindchange="comment" name="comment">
		            <view class="picker_comment">
		              <view class="attr_value">
	 
		                <radio color='' value='一体化'></radio>
		                <label class='radio_label'>一体化</label>
		              </view>
		              <view class="attr_value">
		                <radio color='' value='白卡'></radio>
		                <label class='radio_label'>白卡</label>
		              </view>
		            </view>
		            <view class="picker_comment">
		              <view class="attr_value">
		                <radio color='' value='危险品'></radio>
		                <label class='radio_label'>危险品</label>
		              </view>
		              <view class="attr_value">
		                <radio color='' value='' checked='无(默认)'></radio>
		                <label class='radio_label'>无(默认)</label>
		              </view>
		            </view>
		          </radio-group>
		        </view>


		
	</view>
	
	</view>
</template>

<script>
	import firsthead from '../../components/firsthead/firsthead.vue'
	export default{
		data() {
			return {
				    comment: '',
			}
		},
		components : {
			firsthead
		},
		onLoad() {
			
		},
		methods: {
			
			

		},
		  comment: function(e) {
		    this.setData({
		      comment: e.detail.value,
		    })
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
		margin-left: 120rpx;
	}
	.card-head{
		width: 100%;
		height: 100rpx;
	}
	.shuqian{
		float: right;
		width: 100rpx;
		height: 50rpx;
		background-color: aqua;
		color: blue;
		border-bottom-left-radius:50rpx;
		border-top-left-radius:50rpx;
	}
	
	
	
	.text {
	  width: 20%;
	  margin-top: 6rpx;
	  float: left;
	  text-align: center;
	}
	.picker_comment {
	  width: 65%;
	  margin-left: 20%;
	}
	.attr_value {
	  float: left;
	  width: 40%;
	  height: 50rpx;
	  margin-bottom: 20rpx;
	  margin-left: 14rpx;
	  margin-right: 25rpx;
	  position: relative;
	}
	 
	.radio_label {
	  display: block;
	  text-align: center;
	  line-height: 50rpx;
	}
	 
	radio {
	  box-sizing: border-box;
	  background: none;
	  position: absolute;
	  width: 100%;
	  height: 100%;
	  top: 0;
	  left: 0;
	}
	 
	/* radio未选中时样式 */
	 
	radio .wx-radio-input {
	  margin-right: 15rpx;
	  position: absolute;
	  width: 100%;
	  height: 100%;
	  top: 0;
	  left: 0;
	  background: none;
	  border-radius: 6rpx;
	  box-sizing: border-box;
	}
	 
	/* 选中后的 背景样式 （红色背景 无边框 可根据UI需求自己修改） */
	 
	radio .wx-radio-input.wx-radio-input-checked {
	  background-color: transparent;
	  border-color: #01c2ab;
	  overflow: hidden;
	  box-sizing: border-box;
	}
	 
	/* 选中后的 对勾样式 （白色对勾 可根据UI需求自己修改） */
	 
	radio .wx-radio-input.wx-radio-input-checked::before {
	  font-size: 0rpx; /* 对勾大小 去掉 */
	}

</style>
