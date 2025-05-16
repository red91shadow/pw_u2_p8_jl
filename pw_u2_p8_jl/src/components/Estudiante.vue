<template>
  <div class="container">
    <label for="id_nombre">Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
    <label for="id_apellido">Apellido:</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <button v-on:click="agregarEstudiante()">Agregar Estudiantes</button>
    {{ nuevoNombre }}
    <!-- vincular los datos de entrada de un html con una propiedad Reactiva, el arhivo javascript funge como un controlador ..... -->
    <ul>
      <li v-for="{ nombre, apellido } in lista" :key="nombre">
        Nombre: {{ nombre }} - Apellido: {{ apellido }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "Nuevo",
      nuevoApellido: "Nuevo",
      lista: [
        { nombre: "Joel", apellido: "Luna" },
        { nombre: "Pedro", apellido: "Luna" },
        { nombre: "Daniel", apellido: "Teran" },
        { nombre: "carlo", apellido: "Luna" },
        { nombre: "Andrea", apellido: "Luna" },
        { nombre: "ana", apellido: "Tobar" },
        { nombre: "viviana", apellido: "Lopez" },
      ],
    };
  },

  methods: {
    agregarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
      };
      //this.lista.unshift();
      this.lista.push(nuevo);
    },
  },
};
</script>

<style></style>
