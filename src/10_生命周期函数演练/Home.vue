<template>
  <div>
    <h2>Home</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  beforeUnmount() {
    console.log('beforeUnmount, 卸载之前')
  },
  unmounted() {
    console.log('unmounted, 卸载后')
  }
}
</script>

<style scoped>

</style>
