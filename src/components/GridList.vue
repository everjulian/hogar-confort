<!-- Grid content.  -->
<template>
  <div class="grid-container">
<!-- With slot, we can insert content.  -->
    <slot>
    </slot>
  </div>
</template>

<!--Component styles.  -->
<style scoped>
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 16px;
  justify-content: center;
  padding: 16px;
}

.grid-container img {
  max-width: 100%;
  height: auto;
  object-fit: contain;
}

/* Responsive styles.*/
@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: 1fr;
    grid-gap: 12px;
    padding: 12px;
  }
}
</style>