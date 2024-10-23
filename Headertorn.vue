<template>
  <header>
    <div class="logo">Sportify</div>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Ofertas</a></li>
        <li><a href="#">Celebridades</a></li>
        <li><a href="#">Pre-venta</a></li>
        <li>
          <a href="#">Más</a>
          <ul class="dropdown">
            <li><a href="#">Limitados</a></li>
            <li><a href="#">Niños</a></li>
            <li><a href="#">Accesorios</a></li>
          </ul>
        </li>
      </ul>
    </nav>
    <div class="actions">
      <a href="#" class="login">Login</a>
      <a href="#" class="cart">Carrito</a>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',  // Cambia el nombre aquí
}
</script>

<style scoped>
/* Estilos para el header */
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #2c3e50;  /* Color más oscuro */
  color: white;
  padding: 1rem 2rem;  /* Espaciado lateral más amplio */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);  /* Sombra sutil */
}

nav ul {
  list-style-type: none;  /* Elimina los puntos de la lista */
  display: flex;  /* Flexbox para alinear horizontalmente */
  padding: 0;
}

nav ul li {
  margin: 0 15px;  /* Espaciado entre enlaces */
}

nav ul li a {
  text-decoration: none;  /* Eliminar subrayado */
  color: white;  /* Color blanco para el texto */
  transition: color 0.3s;  /* Transición suave al cambiar color */
}

nav ul li a:hover {
  color: #1abc9c;  /* Color al pasar el mouse */
}

.actions a {
  margin-left: 20px;  /* Espaciado entre los botones de acción */
  text-decoration: none;  /* Eliminar subrayado */
  color: white;  /* Color blanco para los botones */
  transition: color 0.3s;  /* Transición suave al cambiar color */
}

.actions a:hover {
  color: #1abc9c;  /* Color al pasar el mouse */
}

/* Dropdown styles */
.dropdown {
  display: none;  /* Ocultar por defecto */
  position: absolute;  /* Posicionamiento absoluto */
  background-color: #2c3e50;  /* Mismo fondo que el header */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);  /* Sombra sutil */
  z-index: 1;  /* Asegura que esté en el frente */
}

nav ul li:hover .dropdown {
  display: block;  /* Mostrar al pasar el mouse */
}

.dropdown li {
  margin: 0;  /* Sin margen */
}

.dropdown li a {
  padding: 10px 15px;  /* Espaciado interno */
  display: block;  /* Hacer que el enlace ocupe todo el espacio */
}
</style>

