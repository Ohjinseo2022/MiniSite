<template>
  <div class="appview">
    <Header />

    <router-view />
  </div>
</template>
<script>
import Header from './components/layout/header.vue'
export default {
  components: { Header }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-weight: bold;
  font-size: 16px;
  background: inherit;
}
</style>
