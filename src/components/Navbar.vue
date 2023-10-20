<template>
    <header>
      <nav>
        <RouterLink to="/" class="topic">Home</RouterLink>
        <RouterLink to="/blog" class="topic">Blog</RouterLink>
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
        font-size: 50px;
        padding: 15px 50px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .topic{
        color: #F8F7FF;
        text-decoration: none;
        margin: 12px;
        transition: .5s;
    }

    .topic:hover{
        color: #000;
    }

</style>