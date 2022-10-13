<template>
	<view>
		
		<chat-text-list my_image="../../static/image/头像.jpg"
		other_image="https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=1429264363,3038688244&fm=26&gp=0.jpg"
		my_name="我的名字"
		other_name="对方的名字"
		v-bind:msgs="msg"
		@send="sendmsg">
		</chat-text-list>
	</view>
</template>

<script>
	import ChatTextList from "@/components/chat-list/chat-text-list.vue";
	
	export default {
		data() {
			return {
				msg:[{me:false, msg:"快出来耍"},
				{me:true, msg:"马上"},
				{me:true, msg:"等一下我，我穿个鞋子"},
				{me:true, msg:"快看，天上有好多只鸽子"},
				{me:false, msg:"哈哈哈哈哈我也看到了，刚接到它们掉下的羽毛了！"},
				{me:true, msg:"哇，羡慕！"},
				{me:false, msg:"1"},
				{me:true, msg:"2"},
				{me:true, msg:"3"},
				{me:false, msg:"4"},
				{me:false, msg:"5"},
				{me:true, msg:"6"},
				{me:true, msg:"6"},
				{me:true, msg:"6"},
				{me:false, msg:"6"},],
			}
		},
		components: {ChatTextList},
		methods: {
			sendmsg(send){
			    console.log("你发送了一条消息"+send)
			}
		}
	}
	
	
	
	
</script>

<style>

</style>
