<template>
  <div class="app">
    <h2 ref="title" :style="{ color: titleColor }">{{ message }}</h2>
    <button ref="btn" @click="changeTitle">修改title</button>

    <Banner ref="banner"></Banner>
  </div>
</template>

<script>
import Banner from './Banner.vue'
export default {
  components: {
    Banner
  },
  data() {
    return {
      message: 'Hello World',
      titleColor: 'red'
    }
  },
  methods: {
    changeTitle() {
      // 1.不要主动的获取DOM并修改DOM内容
      this.message = 'Hello ref'
      this.titleColor = 'skyblue'

      // 2.获取h2/button元素
      console.log(this.$refs.title)
      console.log(this.$refs.btn)

      // 3.获取banner组件
      console.log(this.$refs.banner)
      // 在父组件中可以主动的调用子组件的对象方法
      this.$refs.banner.bannerClick()

      // 获取banner组件实例后, 获取banner中的元素
      console.log(this.$refs.banner.$el)

      // 如果banner的template有多个根, 拿到的是第一个node节点
      // 注意: 开发中不推荐一个组件中有多个根
      console.log(this.$refs.banner.$el.nextSibling)

      // 4.组件实例还有两个属性(了解)
      console.log(this.$parent, '获取父组件, 此处就在App.vue没有父组件--null')
      console.log(this.$root, '获取根组件')
    }
  }
}
</script>

<style scoped></style>
