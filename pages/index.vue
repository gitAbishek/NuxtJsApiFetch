<template>
    <div>
      <div class="products">
        <div v-for="p in products">
         <ProductCard :product="p" />
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  definePageMeta({
    middleware: "auth"
  })
   const { data: products } = await useFetch('https://fakestoreapi.com/products');
  </script>
  
  <style scoped>
  .products {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 1.25rem;
  }

  .products > div {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
  </style>
  