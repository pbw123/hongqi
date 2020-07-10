<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style lang="scss">
  body{
    background: rgb(241, 241, 241);
  }
  *{
    margin: 0;
    padding: 0;
  }
</style>
