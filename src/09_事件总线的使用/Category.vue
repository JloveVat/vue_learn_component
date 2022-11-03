<template>
  <div>
    <h2>Category</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
import eventBus from './utils/event-bus'

export default {
  data() {
    return {
      message: ''
    }
  },
  created() {
    eventBus.on('jingEvent', this.jingEventHandler)
  },
  // 当该组件被销毁, 移除
  unmounted() {
    console.log('category unmounted')
    eventBus.off('jingEvent', this.jingEventHandler)
  },
  methods: {
    jingEventHandler(name, age, height) {
      console.log('jingEvent事件监听')
      this.message = `name: ${name}, age: ${age}, height: ${height}`
    }
  }
}
</script>

<style scoped></style>
