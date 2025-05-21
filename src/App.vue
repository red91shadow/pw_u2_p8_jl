<template>
  <!-- <HolaMundoView></HolaMundoView> -->
  <!--<Contador-View /> -->
  <EstudianteTablaView/>
</template>

<script>
//import HolaMundoView from "../src/views/HolaMundoView.vue"
//import ContadorView from "../src/views/ContadorView.vue";
//import EstudianteView from "../src/views/EstudianteView.vue";
//import EstudianteTablaViewVue from './views/EstudianteTablaView.vue';
import EstudianteTablaView from "../src/views/EstudianteTablaView.vue";

export default {
  name: "App",
  components: {
    EstudianteTablaView,
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
