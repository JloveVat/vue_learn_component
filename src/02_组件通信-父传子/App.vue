<template>
  <div>
    <ShowInfo name="jing" :age="18" :height="1.77" address="深圳"></ShowInfo>
    <ShowInfo name="you" :age="22"></ShowInfo>
  </div>
</template>

<script>
import ShowInfo from './ShowInfo.vue'

export default {
  components: {
    ShowInfo
  },
  data() {
    return {}
  }
}
</script>

<style scoped></style>
