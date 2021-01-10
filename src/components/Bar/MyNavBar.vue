<template>
    <div id="navbar">
        <van-nav-bar
            left-text="返回"
            left-arrow
            @click-left="returnBack"
            :style="{background: NavBarColor}"
        >
       
        <search-column slot="title"></search-column>
        </van-nav-bar>
    </div>
</template>

<script>
import SearchColumn from 'components/SearchColumn.vue'
export default {
    name: 'MyNavBar',
    data(){
        return{
            NavBarColor: '#536DFE',
        }
    },
    components: {
        SearchColumn
    },

    methods:{
        returnBack(){
            this.$router.back(-1);
        }
    }
}
</script>

<style lang="scss" scoped>
    #navbar{
        /deep/ .van-nav-bar__text{
            color: #ffffff
        }

        /deep/ .van-icon-arrow-left{
            color: #ffffff
        }

        
    }
</style>