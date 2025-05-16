<template>
  <div class="container">
    <label for="id_nombre">Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />

    <label for="id_apellido">Apellido:</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />

    <label for="id_edad">Edad:</label>
    <input v-model="nuevoEdad" id="id_edad" type="text" />

    <label for="id_genero">Genero:</label>
    <input v-model="nuevoGenero" id="id_genero" type="text" />

    <label for="id_carrera">Carrera:</label>
    <input v-model="nuevoCarrera" id="id_carrera" type="text" />

    <button v-on:click="agregarEstudiante()">Agregar Estudiantes</button>
    {{ nuevoNombre }}
    <!-- vincular los datos de entrada de un html con una propiedad Reactiva, el arhivo javascript funge como un controlador ..... -->
    <ul>
      <li
        v-for="{ nombre, apellido, edad, genero, carrera } in lista"
        :key="nombre"
      >
        Estudiante: {{ nombre }} - Apellido: {{ apellido }} - Edad: {{ edad }} -
        Genero: {{ genero }} - Carrera: {{ carrera }}
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
      nuevoEdad: "Nuevo",
      nuevoGenero: "Nuevo",
      nuevoCarrera: "Nuevo",

      lista: [
        {
          nombre: "Joel",
          apellido: "Luna",
          edad: 21,
          genero: "M",
          carrera: "Ingeniería",
        },
        {
          nombre: "Pedro",
          apellido: "Pascal",
          edad: 22,
          genero: "M",
          carrera: "Arquitectura",
        },
        {
          nombre: "Daniel",
          apellido: "Teran",
          edad: 20,
          genero: "M",
          carrera: "Derecho",
        },
      ],
    };
  },

  methods: {
    agregarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
        edad: this.nuevoEdad,
        genero: this.nuevoGenero,
        carrera: this.nuevoCarrera,
      };
      //this.lista.unshift();
      this.lista.push(nuevo);
    },
  },
};
</script>

<style></style>
