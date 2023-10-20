<template>
  <main>
    
    <InfoCard />

    <section>
      <h1>Technologies</h1>
      <div class="badges">
        <Badge :src="src" :alt="Teste" />
        <Badge :src="src2" :alt="Teste" />
        <Badge :src="src3" :alt="Teste" />
      </div>
    </section>

    <section>
      <h1>Tools</h1>
      <div class="badges">
        <Badge :src="src4" alt="Teste" />
        <Badge :src="src5" alt="Teste" />
        <Badge :src="src6" alt="Teste" />
        <Badge :src="src7" alt="Teste" />
      </div>
    </section>

    <section>
      <h1>Skills</h1>
      <div class="badges">
        <Badge src="/img/teamwork.png" alt="Teamwork"/>
        <Badge src="/img/leadership.png" alt="Leadership"/>
      </div>
    </section>

    <section>
      <h1>Experiences</h1>

      <carousel :items-to-show="3.95" :wrap-around="true" :transition="500">
        <slide v-for="slide in 10" :key="slide">
          <ExperienceCard />
        </slide>

        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </section>

  </main>
</template>

<script>
  import InfoCard from '../components/InfoCard.vue';
  import Badge from '../components/Badge.vue';
  import ExperienceCard from '../components/ExperienceCard.vue';
  import 'vue3-carousel/dist/carousel.css';
  import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

  export default{
    name: "Home",
    components: {
      InfoCard,
      Badge,
      ExperienceCard,
      Carousel,
      Slide,
      Pagination,
      Navigation,
    },
    data() {
      return {
        src: "https://skills.thijs.gg/icons?i=c",
        src2: "https://skills.thijs.gg/icons?i=python",
        src3: "https://skills.thijs.gg/icons?i=javascript",
        src4: "https://skills.thijs.gg/icons?i=docker",
        src5: "https://skills.thijs.gg/icons?i=git",
        src6: "https://skills.thijs.gg/icons?i=github",
        src7: "https://skills.thijs.gg/icons?i=aws",
      }
    }
  }


  
</script>

<style>
  .badges{
    display: flex;
    flex-direction: row;
  }

  .experiences{
    display: flex;
    flex-direction: row;
  }

  .carousel__slide {
    padding: 5px;
  }

  .carousel__viewport {
    perspective: 2000px;
  }

  .carousel__slide--sliding {
    transition: 0.5s;
  }

  .carousel__slide {
    opacity: 0.9;
    transform: scale(0.9);
  }

  .carousel__slide--active ~ .carousel__slide {
    transform: scale(0.9);
  }

  .carousel__slide--active {
    opacity: 1;
    transform: rotateY(0) scale(1.0);
  }
</style>

