<template>
  <div id="app">
    
    <TheHeader></TheHeader>
    <ExternalLinks></ExternalLinks>
    <TheMain></TheMain>
    <TheFooter></TheFooter>

  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import ExternalLinks from './components/ExternalLinks.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';

export default {
    name: "App",
    components: { TheHeader, ExternalLinks, TheMain, TheFooter }
}
</script>

<style lang="scss" scoped>
@import "./assets/scss/_variables.scss";

#app {
  font-family: 'Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
