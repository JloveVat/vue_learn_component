<template>
  <div>
    <Home></Home>
    <h2>{{ message }}</h2>

    <button @click="message = 'app hello'">修改message</button>
  </div>
</template>

<script>
import {computed} from 'vue'
import Home from './Home.vue'
export default {
  components: {
    Home
  },
  data() {
    return {
      message: 'hello app'
    }
  },
  // provide: {
  //   name: 'jing',
  //   age: 22,
  // }

  // 使用data中的属性, provide要写成函数, 一般都是函数
  provide() {
    return {
      name: 'jing',
      age: 22,
      // message: this.message,   // 此处不是响应式, 

      // vue中引入computed函数, 使用computed函数让其值变为响应式
      message: computed(() => this.message)
    }
  }
}
</script>

<style scoped></style>
