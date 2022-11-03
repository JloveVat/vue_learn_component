<template>
  <button @click="bannerBtnClick">bannerClick</button>
</template>

<script>
import eventBus from './utils/event-bus';
export default {
  data() {
    return {}
  },
  methods: {
    bannerBtnClick() {
      console.log('bannerBtnClick');
      eventBus.emit('jingEvent', 'jing', 22, 1.77)
    }
  }
}
</script>

<style scoped></style>
