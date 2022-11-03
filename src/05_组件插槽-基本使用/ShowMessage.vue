<template>
  <div>
    <h2>{{ title }}</h2>
    <div class="content">
      <slot>
        <p>默认插槽中的内容</p>
      </slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: '默认标题'
    },
    content: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped></style>
