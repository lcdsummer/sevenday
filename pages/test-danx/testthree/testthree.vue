<template>
	<view class='text_main1'>
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
</template>

<script>
	
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

<style >
.text_main1{
  font-size: 30rpx;
  color: #495060;
  width: 100%;
  height: 130rpx;
  margin: 30rpx auto;
  margin-left: 30rpx;
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
 
uni-radio .uni-radio-input.uni-radio-input-checked{
		background-color: #248067!important;
		border-color: #248067!important;
		background-clip: content-box!important;
		padding: 6rpx!important;
		box-sizing: border-box;
	}
	
	/* radio 选中后的图标样式*/
	uni-radio .uni-radio-input.uni-radio-input-checked::before{
		display: none!important;
	}

</style>
