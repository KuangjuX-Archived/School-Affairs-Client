
<template>
  <div class="app-container">
    <div class="layout-content">
      <keep-alive v-if="$route.meta.keepAlive">
        <router-view></router-view>
      </keep-alive>
      <router-view v-else></router-view>
    </div>
  </div>
</template>

<script>
import TabBar from '@/components/TabBar'
export default {
  name: 'AppLayout',
  data() {
    return {
     
    }
  },
  components: {
    TabBar
  },
  methods: {
    handleChange(v) {
      console.log('tab value:', v)
    }
  }
}
</script>
