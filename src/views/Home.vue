<template>
  <main>
    <InfoCard />
    <section>
      <h1>Technologies</h1>
      <div class="badges">
        <Badge :src="src" :alt="Teste" />
        <Badge />
        <Badge />
      </div>
    </section>

    <section>
      <h1>Tools</h1>
      <div class="badges">
        <Badge :src="src2" alt="Teste" />
        <Badge />
        <Badge />
      </div>
    </section>
    <h1>Skills</h1>
    <h1>Experiences</h1>
  </main>
</template>

<script setup>
  import InfoCard from '../components/InfoCard.vue';
  import Badge from '../components/Badge.vue';

  const src = "https://skills.thijs.gg/icons?i=c";
  const src2 = "https://skills.thijs.gg/icons?i=docker";
  
</script>

<style>
  .badges{
    display: flex;
    flex-direction: row;
  }
</style>

