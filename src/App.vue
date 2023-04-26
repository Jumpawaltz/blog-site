<template>
  <div>
    <h1>title</h1>
    <Icon type="blog"></Icon>
  </div>
</template>

<script>
import Icon from './components/Icon.vue';
export default {
  name: 'App',
  components: {
    Icon
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
