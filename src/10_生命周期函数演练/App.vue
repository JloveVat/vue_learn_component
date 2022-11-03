<template>
  <div>
    <h2>{{ message }} - {{ counter }}</h2>
    <button @click="message = '新message'">修改message</button>
    <button @click="counter++">+1</button>
    <hr>
    <div>
      <button @click="isShowHome = !isShowHome">显示隐藏Home</button>
      <Home v-if="isShowHome"></Home>
    </div>
  </div>
</template>

<script>
import Home from './Home.vue'
export default {
  components: {
    Home
  },
  data() {
    return {
      message: '初始message',
      counter: 0,
      isShowHome: true
    }
  },
  beforeCreate() {
    console.log('beforeCreate')
  },
  created() {
    console.log('created, 组件被创建完成')
    console.log('1.发送网络请求, 请求数据')
    console.log('2.监听eventBus事件')
    console.log('3.监听watch数据')
  },
  beforeMount() {
    console.log('beforeMount')
  },
  mounted() {
    console.log('mounted')
    console.log('1.获取DOM')
    console.log('2.使用DOM')
  },
  // 数据改变, 界面还没更新
  beforeUpdate() {
    console.log('beforeUpdate')
  },
  updated() {
    console.log('updated')
  },
  beforeUnmount() {
    console.log('beforeUnmount, 卸载之前')
  },
  unmounted() {
    console.log('unmounted, 卸载后')
  }
}
</script>

<style scoped></style>
