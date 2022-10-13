<template>
	<view>
	<uni-nav-bar 
	left-icon="arrowleft" 
	title="编辑学生信息" 
	right-text="确定" 
	backgroundColor="#eee"
	height="140rpx"
	@clickLeft="back"  
	@clickTitle="clickTitle" 
	@clickRight="showMenu"/>
	</view>

</template>

<script>
	export default {
			components: {},
			data() {
				return {}
			},
			methods: {
				back() {
					uni.navigateBack({
						delta: 1
					})
				},
				showMenu() {
					uni.showToast({
					title: '确认'
					})
				},
				
				clickTitle() {
	 
					uni.showToast({
						title: '点击了标题'
					})
				}
			}
		}

</script>

<style scoped>

</style>