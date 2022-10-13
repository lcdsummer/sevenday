<template>
    <view>
        <view class="uni-list">
            <checkbox-group>
                <label @change="choseprofrom(index)" class="uni-list-cell" :class="{'selected':flag==index}" v-for="(item,index) in items" :key="index">
                    <view>
                        <checkbox :checked="item.checked" />
                    </view>
                    <view>{{item.name}}</view>
                </label>
            </checkbox-group>
        </view>
		<view class="u-select">
				{{selectItem}}
		</view>
    </view>
</template>
<script>
    export default {
        data() {
            return {
				flag: -1,
				selectItem:'',
                items: [{
                        value: 'USA',
                        name: '美国'
                    },
                    {
                        value: 'CHN',
                        name: '中国',
                    },
                    {
                        value: 'BRA',
                        name: '巴西'
                    },
                    {
                        value: 'JPN',
                        name: '日本'
                    },
                    {
                        value: 'ENG',
                        name: '英国'
                    },
                    {
                        value: 'FRA',
                        name: '法国'
                    }
                ]
            }
        },
        methods: {
            choseprofrom:function (index) {
            	this.flag = index;
            }
            
        }
    }
</script>

<style>
	.selected {
		color: white;
		background-color: #FC8C06;
	}
.uni-list {
	display: flex;
	flex-direction: row;
}
.uni-list-cell {
	display: flex;
	flex-direction: row;
    /* justify-content: flex-start */
}
</style>
