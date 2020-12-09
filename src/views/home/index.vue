<!-- home -->
<template>
  <div class="index-container">
    <nav-bar></nav-bar>
    <tab-bar></tab-bar>
  </div>
  
</template>

<script>
import TabBar from '../../components/TabBar'
import NavBar from '../../components/MyNavBar'

export default {
  components: {
    TabBar,
    NavBar
  },
  
  data(){
    return {}
  },
  computed: {},

  mounted() {},

  methods: {}
}
</script>
<style lang="scss" scoped></style>
