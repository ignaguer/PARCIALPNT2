<template>
   <div class="container mt-3">
    <div class="jumbotron">
      <Formulario />
    </div>
  </div>
</template>

<script>


import Formulario from './componentes/Formulario.vue'
export default {
  name: 'App',
  components: {
    Formulario
   
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
