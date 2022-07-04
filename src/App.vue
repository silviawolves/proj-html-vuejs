<template>
  <div id="app">
    
    <button class="settings-btn"><i class="fa-solid fa-gear"></i></button>

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
    components: { TheHeader, ExternalLinks, TheMain, TheFooter },
}
</script>

<style lang="scss" scoped>
@import "./assets/scss/_variables.scss";

#app {
  font-family: 'Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  position: relative;

  .settings-btn {
    margin: 0;
    padding: 0;
    border: none;
    position: fixed;
    left: 0;
    top: 100px;
    background-color: white;
    border: 1px solid $btn-grey;
    border-radius: 0 50px 50px 0;
    color: $secondary;
    font-size: 1rem;

      i {
        padding: .5rem;
      }
  }
}
</style>
