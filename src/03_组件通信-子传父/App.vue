<template>
  <div class="app">
    <h2>当前计数: {{ counter }}</h2>
    <AddCounter @add="addBtnClick"></AddCounter>
    <SubCounter @sub="subBtnClick"></SubCounter>
  </div>
</template>

<script>
import AddCounter from './AddCounter.vue'
import SubCounter from './SubCounter.vue'

export default {
  components: {
    AddCounter,
    SubCounter
  },
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    addBtnClick(count) {
      this.counter += count
    },
    subBtnClick(count) {
      this.counter -= count
    }
  }
}
</script>

<style scoped></style>
