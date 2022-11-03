<template>
  <div class="app">
    <!-- 1. input v-model -->
    <!-- <input type="text" v-model="message" />
    <input type="text" :value="message" @input="message = $event.target.value" /> -->

    <!-- 2.组价的v-model, 默认modelValue -->
    <Counter v-model="appCounter"></Counter>
    <!-- || 等同于 -->
    <Counter :modelValue="appCounter" @update:modelValue="appCounter = $event"></Counter>

    <!-- 3.组件的v-model, 自定义名称counter, 可以绑定多个v-model -->
    <Counter2 v-model:counter="appCounter" v-model:jing="appJing"></Counter2>
  </div>
</template>

<script>
import Counter from './Counter.vue'
import Counter2 from './Counter2.vue'
export default {
  components: {
    Counter,
    Counter2
  },
  data() {
    return {
      message: '',
      appCounter: 100,
      appJing: 'jing'
    }
  }
}
</script>

<style scoped></style>
