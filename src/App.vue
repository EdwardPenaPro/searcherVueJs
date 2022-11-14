<template>
  <div id="app">
    <userName />
  </div>
</template>

<script>
import userName from "./components/userName.vue";

export default {
  name: 'App',
  components: {
    userName
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
