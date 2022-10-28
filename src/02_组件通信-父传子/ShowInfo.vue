<template>
  <div class="infos">
    <h2>姓名: {{ name }}</h2>
    <h2>年龄: {{ age }}</h2>
    <h2>身高: {{ height }}</h2>
  </div>
</template>

<script>
export default {
  // props: ['name', 'age', 'height']
  props: {
    name: {
      type: String,
      required: true,
      default: ''
    },
    age: {
      type: Number,
      default: 0
    },
    height: {
      type: Number,
      default: 1.8
    },

    // 对象类型写默认值时需要 default是函数, 函数返回的值时默认值
    friend: {
      type: Object,
      default: () => ({})
    },
    hobbies: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style scoped>
.infos {
  color: #007fff;
}
</style>
