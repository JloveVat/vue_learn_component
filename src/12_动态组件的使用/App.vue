<template>
  <div class="app">
    <div class="tabs">
      <template v-for="item in tabs" :key="item">
        <button :class="{ active: currentTab === item }" @click="itemClick(item)">{{ item }}</button>
      </template>
    </div>

    <div class="view">
      <!-- 方式一: 使用判断(不推荐) -->
      <!-- <template v-if="currentIndex === 0">
        <Home></Home>
      </template>
      <template v-if="currentIndex === 1">
        <About></About>
      </template>
      <template v-if="currentIndex === 2">
        <Category></Category>
      </template> -->

      <!-- 方式二: 动态组件component -->
      <!-- <component :is="tabs[currentIndex]"></component> -->
      <!-- <component :is="currentTab"></component> -->
      <component name="jingyou" :age="22" @homeClick="homeClick" :is="currentTab"></component>
    </div>
  </div>
</template>

<script>
import Home from './views/Home.vue'
import About from './views/About.vue'
import Category from './views/Category.vue'
export default {
  components: {
    Home,
    About,
    Category
  },
  data() {
    return {
      tabs: ['home', 'about', 'category'],
      // currentIndex: 0,
      currentTab: 'home'
    }
  },
  methods: {
    itemClick(tab) {
      // this.currentIndex = index
      this.currentTab = tab
    },
    homeClick(payload) {
      console.log('homeClick: ', payload)
    }
  }
}
</script>

<style scoped>
.active {
  background-color: #00abff;
  color: #fff;
}
</style>
