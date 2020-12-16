<!-- home -->
<template>
  <div class="index-container">
    <nav-bar></nav-bar>
    <label-bar></label-bar>
    <div v-for = "(question, index) in questions" :key="index">
        <question-card :question="question"></question-card>
    </div>
    <tab-bar></tab-bar>
  </div> 
  
</template>

<script>
import TabBar from 'components/TabBar/TabBar'
import NavBar from 'components/MyNavBar'
import QuestionCard from 'components/Question/QuestionCard'
import LabelBar from 'components/TabBar/LabelBar'

export default {
  components: {
    TabBar,
    NavBar,
    QuestionCard,
    LabelBar
  },
  
  data(){
    return {
      // When finishing network request, you can convert the key of Object by Helper function
      questions:[
              {
                title: "身价大涨的方便面",
                description: "大一食堂方便面4.5rmb  大三大概5.5  今年6.5  涨疯了",
                likes: 100,
                comments: 100
              },
              {
                title: "测试",
                description: "测试测试",
                likes: 0,
                comments: 0
              }
            ]
    }
  },
  computed: {},

  mounted() {},

  methods: {}
}
</script>
<style lang="scss" scoped></style>
