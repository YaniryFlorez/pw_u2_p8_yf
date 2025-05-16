<template>
  <div class="container">
    <label for="id_nombre">Nombre</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
    <label for="id_apellido">Apellido</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <label for="id_fecha_nacimiento">Fecha Nacimiento</label>
    <input v-model="nuevaFecha" id="id_fecha_nacimiento" type="date" />
    <label for="id_genero">Genero</label>
    <input v-model="nuevoGenero" id="id_genero" type="text" />
    <label for="id_cedula">Cedula</label>
    <input v-model="nuevaCedula" id="id_cedula" type="text" />
    <button v-on:click="agragarEstudiante()">Agregar Estudiante</button>

    {{ nuevoNombre }}

    <ul>
      <li v-for="{ nombre, apellido, fecha, genero, cedula } in lista" :key="nombre">
        Nombre:{{ nombre }}-Apellido:{{ apellido }}-
        Fecha Nacimiento:{{ fecha }}-Genero:{{ genero }}-
        Cedula:{{ cedula }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "nuevo",
      lista: [
        { nombre: "Yaniry", apellido: "Florez" },
        { nombre: "Daniel", apellido: "Lopez" },
        { nombre: "Pedro", apellido: "Ruiz" },
        { nombre: "Andrea", apellido: "Rivera" },
        { nombre: "Carlos", apellido: "Vargas" },
        { nombre: "Ana", apellido: "Enriquez" },
        { nombre: "Viviana", apellido: "Lopez" },
      ],
    };
  },
  methods: {
    agragarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
        fecha: this.nuevaFecha,
        genero: this.nuevoGenero,
        cedula: this.cedula,

      };
      this.lista.unshift(nuevo);
    },
  },
};
</script>

<style>
</style>