<template>
  <div class="grid-container">
    <slot></slot>
  </div>
</template>

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

@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: 1fr;
    grid-gap: 12px;
    padding: 12px;
  }
}
</style>