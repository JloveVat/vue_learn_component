<template>
  <div class="app">
    <div class="tabs">
      <template v-for="item in tabs" :key="item">
        <button :class="{ active: currentTab === item }" @click="itemClick(item)">{{ item }}</button>
      </template>
    </div>

    <div class="view">
      <!-- include: 组件中的name属性, 指定哪些可以缓存(string|RegExp|Array), string: 逗号分开不能有空格 -->
      <!-- exclude: 排除哪些组件(string|RegExp|Array) -->
      <!-- max: number|string  表示最大缓存多少实例, 一旦达到这个数字, 缓存组件中最近没有访问的实例会被销毁 -->
      <KeepAlive include="home,about">
        <component :is="currentTab"></component>
      </KeepAlive>
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
