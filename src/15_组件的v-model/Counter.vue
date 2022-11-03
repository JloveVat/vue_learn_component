<template>
  <div>
    <h2>Counter: {{ modelValue }}</h2>
    <button @click="changeCounter">修改Counter</button>
  </div>
</template>

<script>
export default {
  props: {
    modelValue: {
      type: Number,
      default: 0
    }
  },
  emits: ['update:modelValue'],
  data() {
    return {}
  },
  methods: {
    changeCounter() {
      console.log(1213)
      this.$emit('update:modelValue', 999)
    }
  }
}
</script>

<style scoped></style>
