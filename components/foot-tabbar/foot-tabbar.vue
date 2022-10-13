<template>
    <cover-view class="tabbar" :style="{'padding-bottom': paddingBottomHeight + 'rpx'}">
        <cover-view class="tabbar-item"
            v-for="(item, index) in list" 
            :key="index" 
            @click="tabbarChange(item.path)"
        >
		<!--	<block v-if="index == 2">
				<cover-image class="item-img item-img2" :src="item.icon_a" v-if="current == index"></cover-image>
				<cover-image class="item-img item-img2" :src="item.icon" v-else></cover-image>
			</block>
			<block v-else>
				<cover-image class="item-img" :src="item.icon_a" v-if="current == index"></cover-image>
				<cover-image class="item-img" :src="item.icon" v-else></cover-image>
			</block>
			-->
			<cover-view class="item-behind" :class="{'tabbarbehind': current == index}" v-if="item.text">
				<cover-view class="item-name" :class="{'tabbarActive': current == index}" v-if="item.text">{{item.text}}</cover-view>
			</cover-view>
            
			
        </cover-view>
    </cover-view>
</template>

<script>
export default {
    props: {
        current: String
    },
    data() {
        return {
            paddingBottomHeight: 0,  //苹果X以上手机底部适配高度
            list: [{
                    text: '课堂',  
                   // icon: '/static/foot-1-d.png',  //未选中图标
                    //icon_a: '/static/foot-1-a.png',  //选中图片
                    path: "/pages/search/search",  //页面路
                },{
                    text: '学习',
                   // icon: '/static/foot-2-d.png',
                   // icon_a: '/static/foot-2-a.png',
                    path: "/pages/addstudent/addstudent",
                }
                ,{
                    text: '私信',
                   // icon: '/static/foot-4-d.png',
                   // icon_a: '/static/foot-4-a.png',
                    path: "/pages/main-login/main-login",
                },{
                    text: '我的',
                   // icon: '/static/foot-5-d.png',
                  //  icon_a: '/static/foot-5-a.png',
                    path: "/pages/my/my",
                },
            ]
        };
    },
    created() {
        let that = this;
        uni.getSystemInfo({
            success: function (res) {
                let model = ['X', 'XR', 'XS', '11', '12', '13', '14', '15'];
                model.forEach(item => {
                    //适配iphoneX以上的底部，给tabbar一定高度的padding-bottom
                    if(res.model.indexOf(item) != -1 && res.model.indexOf('iPhone') != -1) {
                        that.paddingBottomHeight = 40;
                    }
                })
            }
        });
    },
    watch: {
        
    },
    methods: {
        tabbarChange(path) {
            // this.$pageTo.toTab(path);
            uni.switchTab({
                url: path
            })
        }
    }
};
</script>

<style lang="scss" scoped>
   // .tabbarActive{
   //     color: red !important;
   // }
	.tabbarbehind{
		background-color: #02a7f0 !important;
	}
    .tabbar{
        position: fixed;  //固定定位，窗口动了它也不动
        bottom: 10rpx;
        left: 0;
        right: 0;
        width: 100%;
        height: 120rpx;
        background-color: white;
		box-shadow: 0px -4px 10px rgba(0, 0, 0, .2);
        display: flex;  //弹性布局
        justify-content: space-around;
        align-items: center;
        .tabbar-item{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100rpx;
   //          .item-img{
   //              width: 46rpx;
   //              height: 46rpx;
   //              margin-bottom: 4rpx;
   //          }
			// .item-img2{
			// 	width: 66rpx;
			// 	height: 66rpx;
			// }
			.item-behind{
				width: 70rpx;
				height: 70rpx;
				border-radius: 50%;
				border: 1px #b1b1b1 solid;
			}
            .item-name{
				margin-left: 10rpx;
				margin-top: 20rpx;
                font-size: 25rpx;
                color: black;
            }
        }
    }
</style>
