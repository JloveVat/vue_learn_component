<template>
  <div class="content">
    这是内容组件, 下面是内容list
    <AppContentList></AppContentList>
  </div>
</template>

<script>
import AppContentList from './AppContentList.vue'

export default {
  components: {
    AppContentList
  }
}
</script>

<style scoped>
.content {
  background-color: #007fff;
}
</style>
