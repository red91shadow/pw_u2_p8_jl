<template>
  <!-- <HolaMundoView></HolaMundoView> -->
  <!--<Contador-View /> -->
  <!-- <EstudianteTablaView/> -->
  <Formulario5View />
</template>

<script>
import Formulario5View from "../src/views/Formulario5View.vue";
//import HolaMundoView from "../src/views/HolaMundoView.vue"
//import ContadorView from "../src/views/ContadorView.vue";
//import EstudianteView from "../src/views/EstudianteView.vue";
//import EstudianteTablaViewVue from './views/EstudianteTablaView.vue';
//import EstudianteTablaView from "../src/views/EstudianteTablaView.vue";

export default {
  name: "App",
  components: {
    Formulario5View,
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
