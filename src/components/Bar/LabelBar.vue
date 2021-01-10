<template>
  <div id="label-bar">
    <div class="tag-box">
      <div class="tag-item" v-for="(item, index) in showList" :key="index" @click="handelTagChange(item.id)">
        <span :class="{ wordRoll: wordControl(item.name) }">{{ item.name }}</span>
      </div>
    </div>
    <div id="collaspe" @click="handleCollaspe">
        <span v-if="!showMore"><van-icon name="arrow-down" /></span>
        <span v-else><van-icon name="arrow-up" /></span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentTag: 0,
      showMore: false,
      showList: [],
      tagList: [
        {
          id: 1,
          name: '单纯吐槽'
        },
        {
          id: 2,
          name: '党办校办'
        },
        {
          id: 3,
          name: '组织部'
        },
        {
          id: 4,
          name: '宣传部'
        },
        {
          id: 5,
          name: '学工部'
        },
        {
          id: 6,
          name: '校工会'
        },
        {
          id: 7,
          name: '我是一个长长长长标签'
        },
        {
          id: 8,
          name: '我是一个长长长长标签'
        }
      ]
    }
  },

  methods: {
    handelTagChange(i) {
      this.currentTag = i
    },
    handleCollaspe() {
      this.showList = []
      let tmp = this.showMore
      this.showMore = !tmp
      if (this.showMore) {
        this.showList = this.tagList
      } else {
        for (let i = 0; i < 4; i++) {
          this.showList.push(this.tagList[i])
        }
      }
    },
    wordControl(n) {
      if (n.length > 4) {
        return true
      } else {
        return false
      }
    }
  },
  created() {
    for (let i = 0; i < 4; i++) {
      this.showList.push(this.tagList[i])
    }
  }
}
</script>

<style lang="scss" scoped>
.tag-box {
  margin: 0 10px;
  display: grid;
  grid-template-columns: 25% 25% 25% 25%;
  overflow: hidden;
  .tag-item {
    text-align: center;
    font-size: 14px;
    margin: 5px 10px;
    overflow: hidden;
    span {
      display: inline-block;
      width: 100%;
    }
  }
}
#collaspe {
  text-align: center;
}
.wordRoll {
  white-space: nowrap;
  animation: 4s wordsLoop linear infinite normal;
}
@keyframes wordsLoop {
  0% {
    transform: translateX(30%);
  }
  100% {
    transform: translateX(-130%);
  }
}
</style>
