<template>
    <div id="label-bar">
        <van-tabs type="primary" sticky>
            <van-tab title="单纯吐槽">单纯吐槽</van-tab>
            <van-tab title="党办校办">党办校办</van-tab>
            <van-tab title="组织部">组织部</van-tab>
            <van-tab title="宣传部">宣传部</van-tab>
            <van-tab title="学工部">学工部</van-tab>
            <van-tab title="校工会">校工会</van-tab>
        </van-tabs>
    </div>
</template>

<script>
export default {
    
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