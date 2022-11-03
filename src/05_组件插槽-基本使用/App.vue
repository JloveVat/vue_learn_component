<template>
  <div>
    <!-- 1.内容时button -->
    <ShowMessage title="这是标题" content="这是内容">
      <button>我是按钮元素</button>
    </ShowMessage>

    <!-- 2.内容时超链接 -->
    <ShowMessage>
      <a href="https://cn.vuejs.org/guide/introduction.html" target="_blank">超链接Vue</a>
    </ShowMessage>

    <!-- 3.内容是图片 -->
    <ShowMessage>
      <img src="@/img/1000.jpg" alt="" width="100">
    </ShowMessage>

    <!-- 4.插槽默认值 -->
    <ShowMessage></ShowMessage>
  </div>
</template>

<script>
import ShowMessage from './ShowMessage.vue';
export default {
  components: {
    ShowMessage
  },
  data() {
    return {}
  }
}
</script>

<style scoped></style>
