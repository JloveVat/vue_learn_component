<template>
  <div>
    <h2>Home组件</h2>
  </div>
</template>

<script>
import messageMixin from '../mixins/message-mixin'
export default {
  name: 'home',
  mixins: [messageMixin],
  data() {
    return {
      counter: 0
    }
  },
  created() {
    console.log('home created')
  }
}
</script>

<style scoped></style>
