<template>
	<view>
		<chat-text-list my_image="../../static/image/头像.jpg"
		other_image="https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=1429264363,3038688244&fm=26&gp=0.jpg"
		v-bind:msgs="msg"
		>
		</chat-text-list>
	</view>
</template>

<script>
	import StuMsg from "@/components/stu-msg/stu-msg.vue";
	
	export default {
		data() {
			return {
				msg:[{msg:true, name:"宝贝小刘",school:"望子成龙小学",banji:"一年级",phone:"13000000000"},
				{msg:true, name:"宝贝小黄",school:"望子成龙小学",banji:"一年级",phone:"13000000000"},
				]
			}
		},
		components: {StuMsg},
		methods: {
			
		}
	}
	
	
	
	
</script>

<style>

</style>
