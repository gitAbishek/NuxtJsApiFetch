
<template>
    <div class="error-main">
        <p>{{ error.statusCode }}</p>
    </div>
</template>

<script setup>
defineProps(['error'])
</script>

<style scoped>
</style>