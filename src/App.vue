<template>
  <div id="app">
    
    <TheHeader></TheHeader>
    <TheMain></TheMain>
    <TheFooter></TheFooter>

  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';

export default {
    name: "App",
    components: { TheHeader, TheMain, TheFooter }
}
</script>

<style lang="scss" scoped>
@import "./assets/scss/_variables.scss";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: $primary;
}
</style>
