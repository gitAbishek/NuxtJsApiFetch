<template>
    <div>
        <h1>This is Home Page</h1>
    </div>
</template>

<script setup>
 definePageMeta({
    middleware: "auth"
  })
const {sayHello} = useUtils();
sayHello();
</script>