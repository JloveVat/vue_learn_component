<template>
  <div>
    <!-- 1.tab-control -->
    <TabControl :titles="['衣服', '鞋子', '裤子']" @tabItemClick="tabItemClick"></TabControl>
    <!-- 2.展示内容 -->
    <h2>{{ pageContents[currentIndex] }}</h2>
  </div>
</template>

<script>
import TabControl from './TabControl.vue'
export default {
  components: {
    TabControl
  },
  data() {
    return {
      pageContents: ['衣服页面', '鞋子页面', '裤子页面'],
      currentIndex: 0
    }
  },
  methods: {
    tabItemClick(index) {
      console.log(index, '---')
      this.currentIndex = index
    }
  }
}
</script>

<style scoped></style>
