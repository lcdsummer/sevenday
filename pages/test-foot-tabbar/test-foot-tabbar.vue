<template>
    <view>
        <view-tabbar :current="3"></view-tabbar>
    </view>
</template>

<script>
    import Tabbar from '@/components/foot-tabbar/foot-tabbar.vue'
    export default {
        components: {
            'view-tabbar': Tabbar
        }, 
        onShow() {
            uni.hideTabBar({
                animation: false
            })
        },
    }
</script>


<style>

</style>
