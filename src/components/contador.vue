<template>
  <div class="container">
    <h1>Contador</h1>
    <p>{{ this.numero }}<sup>2</sup>= {{ calCuadrado }}</p>
    <div>
        <button v-on:click="incrementar() ">+1</button>
        <button v-on:click="decrementar() ">-1</button>
    </div>
   
    <!--
    <p>{{ numero+1 }}</p>
    <p>{{ 'Mi nombre es:'+texto }}</p>
    <p>{{ activo }}</p>
    <p>{{ usuario }}</p>
    <p>{{ arreglo }}</p>
    1+1
    {{ 1 + 1 }}
    {{ false ? " es verdaddero" : "es falso" }}-->
  </div>
</template>

<script>
import { computed } from 'vue';

export default {
  data() {
    return {
        //reactivos
      numero: 5,
      texto: 'Yaniry Florez',
      activo: true,
      usuario:{
        nombre: 'Yaniry',
        edad: 28,
        genero: 'Femenino',
      },
      //arreglo
      arreglo: ["amariilo", "azul"],


      
    };
  },
  methods:{
    calcularCuadrado(){
       console.log('entro al metodo');
        return this.numero*this.numero;

    },
    incrementar(){
        this.numero++;
    },
     decrementar(){
        this.numero--;
    },

},
    computed:{
        calCuadrado(){
           console.log('entro al metodo computada');
        return this.numero*this.numero; 
        }
    },
  }
</script>

<style>
</style>