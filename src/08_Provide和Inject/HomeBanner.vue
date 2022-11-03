<template>
  <!-- 使用provide中使用computed函数后返回的是ref, 因此此处message需要.value -->
  <div>HomeBanner: {{ name }} -- {{ age }} -- {{ message.value }}</div>
</template>

<script>
export default {
  data() {
    return {}
  },
  inject: ['name', 'age', 'message']
}
</script>

<style scoped></style>
