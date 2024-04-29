<!-- Content to create cards. -->
<template>
  <div class="product-card">
    <div class="card-image">
      <img :src="product.image" :alt="product.name">
    </div>
    <!-- Here we call the data from the data.json file. -->
    <div class="card-content">
      <h3>{{ product.name }}</h3>
      <p>{{ product.description }}</p>
      <p class="price">{{ product.price }}</p>
    </div>
  </div>
</template>

<script>
//Receive the product object.
export default {
  props: ['product']
}
</script>

<!-- Styles for the cards. -->
<style>
.product-card {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.product-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.card-image {
  position: relative;
  padding-bottom: 60%; 
  overflow: hidden;
}

.card-image img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.product-card:hover .card-image img {
  transform: scale(1.1);
}

.card-content {
  padding: 16px;
  text-align: center;
}

.card-content h3 {
  font-size: 1.2rem;
  margin-bottom: 8px;
}

.card-content p {
  margin-bottom: 8px;
  color: #666;
}

.price {
  font-weight: bold;
  color: #333;
  margin-bottom: 12px;
}
</style>