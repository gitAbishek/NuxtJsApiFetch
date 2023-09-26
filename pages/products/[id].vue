<template>
    <div>
        <p>{{ products.title }}</p>
        <p>{{ product.id }}</p>
    </div>
</template>

<script setup>
  const {id} = useRoute().params

  console.log(id,"id");
  const uri = `https://fakestoreapi.com/products/${id}`

  const {data: products} = await useFetch(uri, {key: id});
</script>

<style scoped>
</style>

