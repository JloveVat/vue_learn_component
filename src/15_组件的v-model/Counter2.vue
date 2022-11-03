<template>
  <div>
    <h2>Counter: {{ counter }}</h2>
    <button @click="changeCounter">修改Counter</button>
    <h3>Jing: {{ jing }}</h3>
    <button @click="changeJing">修改Jing</button>
  </div>
</template>

<script>
export default {
  props: {
    counter: {
      type: Number,
      default: 0
    },
    jing: {
      type: String,
      default: ''
    }
  },
  emits: ['update:counter', 'update:jing'],
  data() {
    return {}
  },
  methods: {
    changeCounter() {
      this.$emit('update:counter', 999)
    },
    changeJing() {
      this.$emit('update:jing', 'you')
    }
  }
}
</script>

<style scoped></style>
