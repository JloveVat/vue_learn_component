<template>
  <div>
    <h2>App Message: {{ message }}</h2>
    <Home></Home>
    <button @click="isShowCategory = false">是否显示Category</button>
    <Category v-if="isShowCategory"></Category>
  </div>
</template>

<script>
import eventBus from './utils/event-bus'
import Home from './Home.vue'
import Category from './Category.vue'
export default {
  components: {
    Home,
    Category
  },
  data() {
    return {
      message: 'Hello App',
      isShowCategory: true
    }
  },
  created() {
    // fetch()

    // 事件监听
    eventBus.on('jingEvent', (name, age, height) => {
      console.log('jingEvent事件监听', name, age, height)
      this.message = `name: ${name}, age: ${age}, height: ${height}`
    })
  }
}
</script>

<style scoped></style>
