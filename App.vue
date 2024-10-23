<template>
  <div id="app">
    <!-- Headertorn component -->
    <Headertorn />

    <!-- Contenido principal de la página -->
    <SportProducts />

    <!-- Footerkaka component -->
    <Footerkaka />
  </div>
</template>

<script>
// Importa los componentes con los nuevos nombres
import Headertorn from './components/Headertorn.vue'
import Footerkaka from './components/Footerkaka.vue'
import SportProducts from './components/SportProducts.vue' // Asegúrate de importar SportProducts

export default {
  name: 'App',
  components: {
    Headertorn,
    Footerkaka,
    SportProducts // Registra el componente aquí
  }
}
</script>

<style>
/* Estilos globales si los necesitas */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #fff;
}
</style>
