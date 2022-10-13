<template>
	<view class='text_main1'>
		<radio-group>
		<view class="radio-botton">
	         <label id="radio-camera1-label" for="radio-choice-h-2a">A</label> 
	    </view>
		<view class="radio-botton">
		     <label id="radio-camera1-label" for="radio-choice-h-2a">B</label> 
		</view>
		<view class="radio-botton">
		     <label id="radio-camera1-label" for="radio-choice-h-2a">C</label> 
		</view>
		<view class="radio-botton">
		     <label id="radio-camera1-label" for="radio-choice-h-2a">D</label> 
		</view>
		</radio-group>
		
		<!--可留-->
		<view class="botton">
			<a v-for="(item,index) in tagList" :key="index" @click="choseprofrom(index)"  :class="{'selected':flag==index}">
				<view class="botton">
				{{item.kins}}
				</view>
			</a>
		</view>
		<!--
		<view class="botton">
			<a v-for="(item,index) in tagList" :key="index" >
				<view class="botton" @click="get()"  :class="[type? 'active' : 'actived']">
				{{item.kins}}
				</view>
			</a>
		</view>
-->
		<uni-data-checkbox selectedColor="red" v-model="hobbies" :localdata="hobby" mode="tag"/>
<!--
<uni-section title="更多样式 - tag" subTitle="使用mode=tag属性使用标签样式" type="line">
			<view class="uni-px-5">
				<view class="text">单选选中：{{JSON.stringify(radio3)}}</view>
				<uni-data-checkbox mode="tag" v-model="radio3" :localdata="sex"></uni-data-checkbox>
			</view>
			<view class="uni-px-5 uni-pb-5">
				<view class="text">多选选中：{{JSON.stringify(checkbox3)}}</view>
				<uni-data-checkbox mode="tag" multiple v-model="checkbox3" :localdata="hobby"></uni-data-checkbox>
			</view>
</uni-section>
-->
	</view>
</template>

<script>
    import uniDataChecklist from '../../../uni_modules/uni-data-checkbox/components/uni-data-checkbox/uni-data-checkbox.vue'
	export default {
		data() {
			return {
				flag: -1,
				tagList:[
					{kins:"A"},
					{kins:"B"},
					{kins:"C"},
					{kins:"D"}
				],
				type: true,
				
			hobbies: [1],
			hobby: [
				{text: '足球',value: 0},
				{text: '篮球',value: 1},
				{text: '游泳',value: 2}
			],
   
			}
		},
		components : {
			uniDataChecklist
		},

		methods: {
			choseprofrom:function (index) {
				this.flag = index;
				
			},
			get() {
			          // 第一种
			           this.type = false
			          // 第二种
			         // this.type = !this.type
			        },
			
  
		},

	}
</script>

<style>

	
	.selected {
		float: left;
		
		border-radius: 50%;
		background-color: #FC8C06;
		text-align: center;
		line-height: 60rpx;
	}

	.radio-botton{
		width: 50rpx;
		height: 50rpx;
		background-color: antiquewhite;
	}
	.botton{
		float: left;
		
		width: 60rpx;
		height: 60rpx;
		text-align: center;
		line-height: 60rpx;
		
		border-radius: 50%;
	}
	.active {
		text-align: center;
		line-height: 60rpx;
		border-radius: 50%;
		float: left;
	      width: 40px;
	      height: 40px;
	      background-color: #eee;
	    }
	
	    .actived {
			text-align: center;
			line-height: 60rpx;
			
			border-radius: 50%;
			float: left;
	      width: 40px;
	      height: 40px;
	      background-color: rgb(255, 127, 138);
	    }

</style>
