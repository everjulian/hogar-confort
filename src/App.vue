<template>
  <!-- Here is the main content. -->
  <div class="container">
    <!-- Navigation bar content. -->
    <nav class="sidebar">
      <div class="nav-header">
        <h2>Categorías</h2>
        <button class="btn-add-category">+</button>
      </div>
      <ul class="nav-menu">
        <li><a href="#" class="nav-link">Inicio</a></li>
        <li><a href="#" class="nav-link">Sofás</a></li>
        <li><a href="#" class="nav-link">Lámparas</a></li>
        <li><a href="#" class="nav-link">Sillas</a></li>
        <li><a href="#" class="nav-link">Contacto</a></li>
      </ul>
    </nav>
    <!-- With this, I proceed to display products.  -->
    <main class="main-content">
      <Products />
    </main>
  </div>
</template>

<!-- Import of ProductsList. -->
<script>
import Products from './components/ProductsList';

export default {
  components: {
    Products
  }
}
</script>

<style>

/* General styles. */
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
  padding: 0;
}

/* Styles for the main content */
.main-content {
  flex-grow: 1;
  padding: 20px;
  background-color: #f5f5f5;
}

.container {
  display: flex;
  min-height: 100vh;
}

/* Styles for the sidebar navigation. */
.sidebar {
  background-color: #333;
  color: #fff;
  width: 220px;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

.nav-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.nav-header h2 {
  margin: 0;
}

.nav-menu {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.nav-link {
  display: block;
  padding: 12px;
  color: #fff;
  text-decoration: none;
  transition: background-color 0.3s ease;
  border-radius: 5px;
  margin-bottom: 8px;
}

.nav-link:hover {
  background-color: #555;
}

.btn-add-category {
  background-color: #555;
  color: #fff;
  border: none;
  padding: 8px 12px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  font-size: 16px;
  font-weight: bold;
}

.btn-add-category:hover {
  background-color: #777;
}


</style>