<template>
    <header>
        Testing
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/blog">Blog</RouterLink>
      </nav>
  </header>
</template>

<script setup>
    import  { RouterLink } from 'vue-router';
</script>

<style scoped>

    header {
        background-color: #B8B8FF;
        color: #F8F7FF;
    }

</style>