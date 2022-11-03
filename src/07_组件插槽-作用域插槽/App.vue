<template>
  <div>
    <!-- 1.tab-control -->
    <TabControl :titles="['衣服', '鞋子', '裤子']" @tabItemClick="tabItemClick"></TabControl>
    <!-- 2.展示内容 -->
    <h2>{{ pageContents[currentIndex] }}</h2>

    <TabControl :titles="['衣服', '鞋子', '裤子']" @tabItemClick="tabItemClick">
      <!-- 通过props获得子组件传的值, props中可能有多个 -->
      <template #default="slotProps">
        {{ slotProps }}
      </template>
    </TabControl>
    <TabControl :titles="['衣服', '鞋子', '裤子']" @tabItemClick="tabItemClick">
      <template #default="props">
        <button>{{ props.item }}</button>
      </template>
    </TabControl>
    <TabControl :titles="['衣服', '鞋子', '裤子']" @tabItemClick="tabItemClick">
      <template #default="props">
        <a href="#">{{ props.item }}</a>
      </template>
    </TabControl>

    <!-- 独占默认插槽简写 -->
    <TabControl :titles="['衣服', '鞋子', '裤子']" @tabItemClick="tabItemClick">
      <template v-slot="props">
        <p>{{ props.item }}省略defalut</p>
      </template>
    </TabControl>

    <!-- 只有一个默认插槽, template可以省略, 组件标签可以当成模板 -->
    <TabControl :titles="['衣服', '鞋子', '裤子']" @tabItemClick="tabItemClick" v-slot="props">
      <p>{{ props.item }}简写</p>
    </TabControl>

    <!-- 如果有多个插槽, 不能简写 -->
  </div>
</template>

<script>
import TabControl from './TabControl.vue'
export default {
  components: {
    TabControl
  },
  data() {
    return {
      pageContents: ['衣服页面', '鞋子页面', '裤子页面'],
      currentIndex: 0
    }
  },
  methods: {
    tabItemClick(index) {
      console.log(index, '---')
      this.currentIndex = index
    }
  }
}
</script>

<style scoped></style>
