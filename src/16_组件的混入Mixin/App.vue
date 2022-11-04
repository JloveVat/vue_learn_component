<template>
  <div>
    <Home></Home>
    <About></About>
    <Category></Category>
  </div>
</template>

<script>
import Home from './views/Home.vue'
import About from './views/About.vue'
import Category from './views/Category.vue'
export default {
  components: {
    Home,
    About,
    Category
  },
  data() {
    return {}
  }
}
</script>

<style scoped></style>
