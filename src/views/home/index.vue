<!-- home -->
<template>
  <div class="index-container">
    <nav-bar></nav-bar>
    <tab-bar></tab-bar>
    <!-- <question-card></question-card> -->
    <div v-for = "(question, index) in questions" :key="index">
        <question-card :question="question"></question-card>
    </div>
  </div> 
  
</template>

<script>
import TabBar from 'components/TabBar'
import NavBar from 'components/MyNavBar'
import QuestionCard from 'components/Question/QuestionCard'

export default {
  components: {
    TabBar,
    NavBar,
    QuestionCard
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
