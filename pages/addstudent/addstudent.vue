<template>
	<view class="five">
		
		<view class="top">
			<!--<text class="iconfont icon-fanhuijiantou"></text>-->
			<firsthead title="新增学生信息"></firsthead>
		</view>
		
		<view class="passage">
			
			<view>
			<view class="photo">
			<view class="left">学生照片</view>
			</view>
			</view>
			<view class="left">学生姓名</view>
			<input type="text" placeholder="请输入学生姓名" placeholder-style="color:#dadada"/>

			<view class="left">学校</view>
			<input type="text" placeholder="请输入学校" placeholder-style="color:#dadada"/>
			
			<view class="left">联系方式</view>
			<input type="text" placeholder="请输入联系方式" placeholder-style="color:#dadada"/>
			
			
			<view>
			<view class="item">
				<view class="select-left">年级</view>
				<i class="iconfont icon-youjiantou-copy"></i>
				<view class="select"><picker mode="selector" @change="bindPickerChange" :range="array" range-key="phone">{{array[index].phone}}</picker></view>
			    
			</view>
		    </view>
		</view>

		<view class="under-passage">
		<view>
			<view  class="under-left">注意事项</view>
			<view  class="under-list" @click="showMore"> {{isShow ? '∧':'∨'}} </view>
			<view  class="show-more" :class="[isShow ? 'show-more-click' : '']">
				<view class="under-test" v-if="isShowText">
				Lorem ipsum dolor sit amet,consectetur adipiscing Lorem ipsum dolor sit amet,consectetur adipiscing Lorem ipsum dolor sit amet,consectetur adipiscing Lorem ipsum dolor sit amet,consectetur adipiscing Lorem ipsum dolor sit amet.
				</view>
			</view>
		</view>
		</view>


	</view>
</template>

<script>
	import firsthead from '../../components/firsthead/firsthead.vue'
	export default {
		data() {
			return {
				array:[{phone:'高三'},{phone:'高二'},{phone:'高一'}],
				index:0,
				
				isShow:this.isShow,
				isShowText:this.isShowText
			}
		},
		components : {
			firsthead
		},
		methods: {
			bindPickerChange(e){
				this.index=e.detail.value
			},
			
			showMore(){
				this.isShow = !this.isShow
				this.isClick = !this.isClick
				
				// 先展开500毫秒后再显示文字,收缩200毫秒后再隐藏文字
				if(this.isShowText){
					setTimeout(()=>{
						this.isShowText = !this.isShowText
					},100)
				}else{
					setTimeout(()=>{
						this.isShowText = !this.isShowText
					},400)
				}
				
			}
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
		width: 570rpx;
		margin-left: 40rpx;
		line-height: 80rpx;
		border-bottom: solid 1rpx #EEEEEE;

	}
	
	.passage{
		background-color: white;
		margin-left: 50rpx;
		width: 660rpx;
		height: 780rpx;
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
		height: 180rpx;
		width: 570rpx;
		margin-bottom: 15rpx;
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
	
	.under-passage::after{
	    content: '';
	    display: table;
	    clear: both;
	}
	
	/* 点击更多的样式 */
	.show-more{
		width: 100%;
		height: 2rpx;
		margin-top: 30rpx;
		float: left;
		border-radius: 50rpx;
		background-color:white;
		transition:height 1s;
		-moz-transition:height 1s; /* Firefox 4 */
		-webkit-transition:height 1s; /* Safari and Chrome */
		-o-transition:height 1s; /* Opera */
	
	}
	
	.under-test{
		margin-top: 65rpx;
		margin-left: 40rpx;
		// position:absolute;
		// z-index: 100;
		
	}
	.show-more-click{
		height: 250px;
	}
	


</style>
