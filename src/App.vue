<template>
  <div id="app">
    <TopBar />
    <TopBanner />
    <HelloWorld msg="Welcome to ChengYi" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TopBar from './components/TopBar.vue';
import TopBanner from './components/TopBanner.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    TopBar,
    TopBanner
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
