<template>
  <div>
    <Pager :total="total" :current="current" @update:current="handlePageChange($event)"></Pager>
  </div>
</template>

<script>
import Pager from "./components/Pager/";
export default {
  data() {
    return {
      total: 120,
      current: 5,
    }
  },
  methods: {
    handlePageChange(newPage) {
      this.current = newPage
    }
  },
  name: 'App',
  components: {
    Pager
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
