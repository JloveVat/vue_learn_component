<template>
  <div class="banner">
    <h2>Banner</h2>
  </div>
  <!-- 最好只有一个根 -->
  <div class="banner2">第二个根</div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    bannerClick() {
      console.log('bannerClick')
    }
  }
}
</script>

<style scoped></style>
