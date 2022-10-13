<template>
	<view class="five">
		
		<view class="top">
			<firsthead/>
		</view>
		
		<view class="passage">
			
			<view>
			<view class="photo">
			<view class="left">学生照片</view>
			<view>
				<open-data type="userAvatarUrl" class="userinfo" id="userinfo">
				<image src="../../static/image/头像.jpg" mode="widthFix"></image>
				</open-data>
			</view>
			</view>
			</view>
			<view class="left">学生姓名</view>
			<input type="text" v-model="stuName"/>

			<view class="left">学校</view>
			<input type="text" v-model="schName"/>
			
			<view class="left">联系方式</view>
			<input type="text" v-model="phone"/>
			
			
			<view>
			<view class="item">
				<view class="select-left">年级</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select"><picker mode="selector" @change="bindPickerChange" :range="array" range-key="phone">{{array[index].phone}}</picker></view>
			    
			</view>
		    </view>
		</view>



	</view>
</template>

<script>
	import firsthead from '../../components/second-head/second-head.vue'
	export default {
		data() {
			return {
				array:[{phone:'高三'},{phone:'高二'},{phone:'高一'}],
				index:0,
				stuName:'小肥猪',
				schName:'魔法学院',
				phone:'13920000000',

			}
		},
		components : {
			firsthead
		},
		methods: {
			bindPickerChange(e){
				this.index=e.detail.value
			},
			
			
		}
	}
</script>

<style lang="scss">
	
	.five{
		width: 750rpx;
		height: 1625rpx;
		background-color: #EEEEEE;
	}

	.item{
		height: 80rpx;
		width: 570rpx;
		line-height: 80rpx;
		margin-left: 40rpx;
		
	}
	
	.left{
		margin-top: 35rpx;
		margin-left: 40rpx;
		float: left;
	
	}
	
	.passage input{
		float: left;
		height: 80rpx;
		width: 555rpx;
		margin-left: 40rpx;
		padding-left: 15rpx;
		margin-top: 10rpx;
		line-height: 80rpx;
		background-color: #eee;
		border-radius: 50rpx;
		

	}
	
	.passage{
		background-color: white;
		margin-left: 50rpx;
		margin-top: 20rpx;
		width: 660rpx;
		height: 800rpx;
		border-radius: 50rpx;
		
	}
	
	.under-passage{
		background-color: white;
		margin-left: 50rpx;
		margin-top: 30rpx;
		width: 660rpx;
		height: 100rpx;
		border-radius: 50rpx;
		position:absolute;
		z-index: 99;
	}
	
	.photo{
		height: 200rpx;
		width: 570rpx;
		margin-bottom: 15rpx;
	}
	
	
	#userinfo{
	  width: 140rpx;
	  height:140rpx;
	  border-radius:50%;
	  display: flex;
	  overflow:hidden;
	  float: left;
	  margin-top: 70rpx;
	  margin-left: 120rpx;
	}
	
	.under-left{
		margin-top: 35rpx;
		margin-left: 40rpx;
		float: left;
		position:absolute;
		z-index: 100;
	}
	
	.select-left{
		margin-top: 15rpx;
		float: left;
	}
	
	.iconfont{
		margin-top: 15rpx;
		float: right;
	}
	.select{
		margin-top: 15rpx;
		width: 100rpx;
		float: right;
		color: #dadada;
	}
	
	.under-list{
		left: 570rpx;
		margin-right: 50rpx;
		margin-top: 30rpx;
		position:absolute;
		z-index: 100;
	}
	
	.passage::after{
	    content: '';
	    display: table;
	    clear: both;
	}
	
	
	
	
	
	


</style>
