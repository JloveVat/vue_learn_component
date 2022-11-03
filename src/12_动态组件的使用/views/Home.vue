<template>
  <div>
    <h2>Home组件: name: {{ name }} --- age: {{ age }}</h2>
    <button @click="homeBtnClick">homeBtn</button>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: ''
    },
    age: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {}
  },
  methods: {
    homeBtnClick() {
      this.$emit('homeClick', 'home')
    }
  }
}
</script>

<style scoped></style>
