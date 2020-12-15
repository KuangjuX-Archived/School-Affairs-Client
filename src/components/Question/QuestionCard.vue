<template>
    <div>
        <van-panel 
        :title=question.title 
        :desc=question.description 
        header-class= "header"
        >
        </van-panel>
    </div>
</template>

<script>
export default {
    data(){},
    props:{
        question: Object
    }
}
</script>

<style lang="scss">
    .header{
        font-size: 20px !important;
        font-weight: 1000 !important;
    }
</style>