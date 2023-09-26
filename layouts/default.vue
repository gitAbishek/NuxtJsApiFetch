<template>
    <div>
      <nav class="navbar">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/contact-us">Contact Us</NuxtLink></li>
      </nav>
    </div>
    <div>
      <slot />
    </div>
  </template>

  <script setup>
</script>

<style scoped>
  .router-link-exact-active{
    color: red;
  }

  .navbar{
    display:flex;
    padding: 10px;
    gap: 20px;
  }

  li {
    list-style: none;
    text-decoration: none;
  }
</style>