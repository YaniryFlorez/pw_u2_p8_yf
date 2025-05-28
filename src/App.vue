<template>
  
  <PokemonView/>
</template>

<script>
/*
import ContadorView from '@/views/ContadorView.vue';
import HolaMundoVue from './views/HolaMundoVue.vue'
import ContadorViewvuevue from '@/views/ContadorView.vue'
import EstudianteView from '@/views/EstudianteView.vue'
import EstudianteTablaView from '@/views/EstudianteTablaView.vue' 
import ProductoView from './views/ProductoView.vue';*/
import PreguntaView from '@/views/PreguntaView.vue';
import PokemonView from '@/views/PokemonView.vue';
export default {
  name: 'App',
  components: {
    //ContadorView,
    //HolaMundoVue,
    //ContadorViewvuevue,
    //EstudianteView,
    //EstudianteTablaView,
    //PreguntaView,
    PokemonView,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3521e6;
  margin-top: 60px;
}
</style>
