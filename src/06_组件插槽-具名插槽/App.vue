<template>
  <div>
    <NavBar>
      <template v-slot:left>
        <button>{{ leftText }}</button>
      </template>
      <!-- 语法糖v-slot是# -->
      <template #center>
        <span>内容</span>
      </template>
      <template #right>
        <a href="#">登陆</a>
      </template>
    </NavBar>

    <NavBar>
      <!-- 动态插槽名 -->
      <template #[position]> 中间内容 </template>
    </NavBar>

    <button @click="position = 'left'">左</button>
    <button @click="position = 'center'">中</button>
    <button @click="position = 'right'">右</button>
  </div>
</template>

<script>
import NavBar from './NavBar.vue'
export default {
  components: {
    NavBar
  },
  data() {
    return {
      position: 'center',
      leftText: '返回按钮'
    }
  }
}
</script>

<style>
body {
  margin: 0;
}
</style>
