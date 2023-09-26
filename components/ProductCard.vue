<template>
    <div class="card">
        <img :src="product.image" alt="product thumb" class="thumb">
        <p>{{ product.title }}</p>
        
        <button @click="handleViewDetails">View Details</button>
    </div>
</template>

<script setup>
   const {id} = useRoute().params
   const router = useRouter()
   const {product} = defineProps(['product'])

   const handleViewDetails  = () => {
    console.log(product.id,"id");
    if (product.id) {
    router.push(`/products/${product.id}`);
  } else {
    console.error('No id parameter found in the route');
  }
   }
</script>

<style scoped>

.thumb {
    max-height: 120px;
    max-width: 70%;
    margin: 0 auto;
}

.card {
    padding: 30px;
    border-radius: 20px;
    background: white;
    height: full;
    box-shadow: 5px 5px 20px 0 rgba(222, 200, 200, 0.2);}
</style>