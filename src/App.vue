<template>
  <div id="app">
    <!-- <userName /> -->
    <!-- <rick-and-morty /> -->
    <rickAndMorty/>
  </div>
</template>

<script>
// import userName from "./components/userName.vue";
import RickAndMorty from './components/rickAndMorty.vue';
export default {
  name: 'App',
  components: {
    // userName,
    RickAndMorty
    
  }
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #4a535c;
  
} */


</style>
