<template>
  <main class="products-content">
    <section class="hero">
      <div class="hero-banner">
        <h1>Bienvenido a Sportify</h1>
        <img src="@/assets/banner-sportify.jpg" alt="Banner Sportify" class="hero-image" /> <!-- Agregada la imagen del banner -->
      </div>
    </section>

    <section class="products">
      <h2>Productos Destacados</h2>
      <div class="product-grid">
        <div class="product-card" v-for="product in products" :key="product.id">
          <img :src="product.image" :alt="product.name" class="product-image"/>
          <h3>{{ product.name }}</h3>
          <p>${{ product.price }}</p>
          <button class="add-to-cart">Añadir al Carrito</button>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'SportProducts',
  data() {
    return {
      products: [
        { id: 1, name: 'Valen Normal', price: 29.99, image: require('@/assets/valennormal.jpg') },
        { id: 2, name: 'Magician', price: 19.99, image: require('@/assets/magician.jpg') },
        { id: 3, name: 'Benja Normal', price: 39.99, image: require('@/assets/benjanormal.jpg') },
        { id: 4, name: 'Benja Chupetín', price: 49.99, image: require('@/assets/benjachupetin.jpg') },
      ],
    };
  },
}
</script>

<style scoped>
/* Estilos para el cuerpo */
.products-content {
  padding: 2rem;
  background-color: #ecf0f1;  /* Color de fondo más claro */
}

.hero {
  text-align: center;
  margin-bottom: 2rem;
  position: relative;
}

.hero-banner {
  position: relative;
  z-index: 1;  /* Asegura que el texto esté por encima de la imagen */
}

.hero-banner h1 {
  font-size: 2.5rem;
  color: #2c3e50;  /* Color del texto */
}

.hero-image {
  width: 800px; /* Ajustar el tamaño del banner */
  height: auto; /* Mantener la proporción */
  margin-top: 1rem; /* Espaciado superior */
}

.products {
  margin-top: 2rem;
}

.products h2 {
  margin-bottom: 1rem;
  text-align: center;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));  /* Responsive grid */
  gap: 1rem;
  justify-items: center; /* Centrar los items */
}

.product-card {
  background-color: white;
  border: 1px solid #ddd;  /* Borde sutil */
  border-radius: 4px;  /* Bordes redondeados */
  padding: 1rem;
  text-align: center;
  transition: box-shadow 0.3s;  /* Transición suave */
}

.product-card:hover {
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);  /* Sombra al pasar el mouse */
}

.product-image {
  width: 150px; /* Ajusta el ancho */
  height: 150px; /* Ajusta la altura */
  object-fit: cover; /* Mantiene la proporción y recorta si es necesario */
  border-radius: 4px; /* Bordes redondeados opcionales */
}

.add-to-cart {
  margin-top: 1rem;
  padding: 0.5rem;
  background-color: #1abc9c;  /* Color del botón */
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;  /* Transición suave */
}

.add-to-cart:hover {
  background-color: #16a085;  /* Color al pasar el mouse */
}
</style>
