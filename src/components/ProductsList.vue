<!-- Here is the main content. -->
<template>
  <div>
    <h1>Listado de productos</h1>
    <Grid>
      <Card v-for="product in products" :key="product.id" :product="product" />
    </Grid>
  </div>
</template>

<!-- Import of the components CardList, GridList, data.json. -->
<script>
import Card from './CardList';
import Grid from './GridList';
import data from '../data.json';

export default {
  components: {
    Card,
    Grid
  },
  data() {
    return {
      products: data
    }
  }
}
</script>
