<template>
    <div id="question-card">
        <van-panel 
        :title=question.title 
        type="primary"
        use-footer-slot
        >
        <div class="description">
            {{question.description}}
        </div>
        <div slot="footer">
            <van-icon name="chat-o" size="25px"/>
            <van-icon name="like-o" size="25px"/>
        </div>
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
    .van-cell__title{
        font-size: 20px !important;
        font-weight: 1000 !important;
    }

    .description{
        font-size: 14px !important;
        font-weight: 300 !important;
        color: #000000 !important;
        margin: 10px 20px 10px 20px !important; 
    }
</style>