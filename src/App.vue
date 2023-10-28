<script setup>
import { RouterView } from 'vue-router';
import Navbar from './components/Navbar.vue';
</script>

<template>
  <Navbar />
  <RouterView />
</template>

<style scoped>
  
  * {
    font-family: monospace;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

</style>
