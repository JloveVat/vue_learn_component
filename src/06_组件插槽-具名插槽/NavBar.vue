<template>
  <!-- 默认没有名字的插槽的名字是default -->
  <div class="nav-bar">
    <div class="left">
      <slot name="left">left</slot>
    </div>
    <div class="center">
      <slot name="center">center</slot>
    </div>
    <div class="right">
      <slot name="right">right</slot>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  }
}
</script>

<style scoped>
.nav-bar {
  display: flex;
  height: 44px;
  line-height: 44px;
  text-align: center;
}

.left {
  width: 80px;
  background-color: #00afff;
}

.center {
  flex: 1;
  background-color: orange;
}

.right {
  width: 80px;
  background-color: skyblue;
}
</style>
