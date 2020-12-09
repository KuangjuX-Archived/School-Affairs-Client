<template>
    <div>
        <van-nav-bar
            left-text="返回"
            left-arrow
            @click-left="returnBack"
        >
       
        <search-column slot="title"></search-column>
        </van-nav-bar>
    </div>
</template>

<script>
import SearchColumn from './SearchColumn.vue'
export default {
    name: 'MyNavBar',
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