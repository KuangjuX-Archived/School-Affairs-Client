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
        <div slot="footer" id="footer">
            <div>
                <van-icon name="chat-o" size="25px"/>
                <span class="question-counts">{{question.comments}}</span>
            </div>
            <div>
                <van-icon name="like-o" size="25px"/>
                <span class="question-counts">{{question.likes}}</span>
            </div>
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
    .van-panel{
        margin: 10px;
        border-radius: 1em;
    }

    .van-panel__header{
        border-radius: 1em 1em 0 0;
    }
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

    #footer{
        display: inline-flex !important;
    }

    #footer div{
        margin:auto 10px auto auto;
        display: inline-flex;
    }

    .question-counts{
        display: block;
        margin: 5px auto auto 5px;
    }
</style>