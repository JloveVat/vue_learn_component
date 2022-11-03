<template>
  <div class="add">
    <button @click="btnClick(-1)">+1</button>
    <button @click="btnClick(5)">+5</button>
    <button @click="btnClick(10)">+10</button>
  </div>
</template>

<script>
export default {
  // emits: ['add'],
  // emits对象写法
  emits: {
    // add: null
    // 做验证, 如果是false控制台会报警告
    add(count) {
      if (count >= 0) {
        return true
      }
      return false
    }
  },
  methods: {
    btnClick(count) {
      this.$emit('add', count)
    }
  }
}
</script>

<style scoped></style>
