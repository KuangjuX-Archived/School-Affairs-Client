<template>
    <div id="label-bar">
        <van-tabs type="primary" sticky @click="handelTag">
            <div v-for="(item, index) in tagLists" :key="index">
                <van-tab :title="item.name"  :name="item.id">{{item.id}}</van-tab>
            </div>
        </van-tabs>
    </div>
</template>

<script>
export default {
    data(){
        return{
            tagLists:[
                {
                    id: 1,
                    name: '单纯吐槽'
                },
                {
                    id: 2,
                    name: '党办校办'
                },
                {
                    id: 3,
                    name: '组织部'
                },
                {
                    id: 4,
                    name: '宣传部'
                },
                {
                    id: 5,
                    name: '学工部'
                },
                {
                    id: 6,
                    name: '校工会'
                }
            ]
        }
    },

    methods:{
        handelTag(name, title){
            console.log("name", name)
            console.log("title", title)
        }
    },

    created(){}
    
}
</script>

<style lang="scss" scoped>
    #label-bar /deep/ .van-tabs__wrap--scrollable .van-tabs__nav--complete{
        height: 40px !important;
    }

    #label-bar /deep/ .van-tabs__content{
        display: none;
    }

    #label-bar /deep/ .van-tab{
        background-color: gray;
        color: #ffffff;
        margin: 0 5px 0 5px;
        border-radius: 5px;
        font-weight: 500;
        font-size: 16px;
    }
</style>