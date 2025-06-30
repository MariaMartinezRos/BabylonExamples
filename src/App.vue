<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <BabylonExample msg="Welcome to Your Vue.js + TypeScript App"/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BabylonExample from './components/BabylonExample.vue';

export default defineComponent({
  name: 'App',
  components: {
    BabylonExample
  }
});
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
