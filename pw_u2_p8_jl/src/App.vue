<template>
  <!-- <HolaMundoView></HolaMundoView> -->
  <Contador-View />
</template>

<script>
//import HolaMundoView from "../src/views/HolaMundoView.vue"
import ContadorView from "../src/views/ContadorView.vue";

export default {
  name: "App",
  components: {
    ContadorView,
  },
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
