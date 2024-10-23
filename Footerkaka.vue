<template>
  <footer>
    <div class="footer-links">
      <div class="socials">
        <a href="https://youtube.com" target="_blank">YouTube</a>
        <a href="https://twitter.com" target="_blank">Twitter</a>
        <a href="https://instagram.com" target="_blank">Instagram</a>
        <a href="https://wa.me" target="_blank">WhatsApp</a>
      </div>
      <div class="info">
        <a href="#">Servicio</a>
        <a href="#">Ayuda</a>
        <a href="#">Acerca de Sportify</a>
      </div>
    </div>
    <div class="search-bar">
      <input type="text" placeholder="Buscar..." />
      <button>Buscar</button>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent',  // Cambia el nombre aquí
}
</script>

<style scoped>
/* Estilos para el footer */
footer {
  background-color: #2c3e50;  /* Mismo color que el header */
  color: white;
  padding: 1rem 2rem;  /* Espaciado lateral más amplio */
}

.footer-links {
  display: flex;
  justify-content: space-between;
}

.socials a {
  margin-right: 15px;  /* Espaciado entre enlaces de redes sociales */
  color: white;  /* Color de texto */
  text-decoration: none;  /* Eliminar subrayado */
  transition: color 0.3s;  /* Transición suave al cambiar color */
}

.socials a:hover {
  color: #1abc9c;  /* Color al pasar el mouse */
}

.info a {
  margin-right: 15px;  /* Espaciado entre enlaces de información */
  color: white;
  text-decoration: none;  /* Eliminar subrayado */
  transition: color 0.3s;  /* Transición suave al cambiar color */
}

.info a:hover {
  color: #1abc9c;  /* Color al pasar el mouse */
}

.search-bar {
  margin-top: 1rem;
  display: flex;  /* Usar flexbox para alinear el campo de búsqueda y el botón */
}

.search-bar input {
  padding: 0.5rem;
  border: none;  /* Sin borde */
  border-radius: 4px;  /* Bordes redondeados */
}

.search-bar button {
  padding: 0.5rem 1rem;
  border: none;  /* Sin borde */
  background-color: #1abc9c;  /* Color del botón */
  color: white;
  border-radius: 4px;  /* Bordes redondeados */
  cursor: pointer;
}

.search-bar button:hover {
  background-color: #16a085;  /* Color del botón al pasar el mouse */
}
</style>
