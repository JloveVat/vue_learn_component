<template>
  <div>
    <h2>Home组件</h2>
    <h3>当前计数: {{ counter }}</h3>
    <button @click="counter++">+1</button>
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      counter: 0
    }
  },
  created() {
    console.log('home created')
  },
  unmounted() {
    console.log('home unmounted')
  },
  // 对于保持了keep-alive组件, 无法进行监听切换, 提供了两个函数
  // keep-alive进入活跃状态
  activated() {
    console.log('home activated')
  },
  // keep-alive离开活跃状态
  deactivated() {
    console.log('home deactivated')
  }
}
</script>

<style scoped></style>
