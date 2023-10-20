<template>
  <main>
    
    <InfoCard />

    <section class="section-class">
      <h1>Introduction</h1>
      <div>
        <p>👋 Hello, there! My name is Filipi and I'm currently graduating in computer engeneer at Inteli.</p>
        <p>I'm {{ age }} years old and looking for opportunities to improve my knowledge and test my skills and limits.</p>
      </div>
    </section>

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
        age: 20
      }
    }
  }


  
</script>

<style scoped>

  .section-class{
    margin: 0 auto;
    text-align: center;
  }

  .section-class p{
    overflow: hidden;
    border-right: .15em solid plum;
    white-space: nowrap;
    margin: 0 auto;
    max-width: fit-content;
    letter-spacing: .15em;
    animation: 
      typing 3.5s steps(40, end),
      blink-caret .75s step-end infinite;
  }

  @keyframes typing{
    from { width: 0 }
    to { width: fit-content;}
  }

  @keyframes blink-caret{
    from, to { border-color: transparent }
    50% { border-color: plum; }
  }

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

  .typewriter p{
    align-content: center;
    justify-content: center;
    align-items: center;
    /* Ensures the content is not revealed until the animation */
    /* border-right: .15em solid orange; The typewriter cursor 
    margin: 0 auto; /* Gives that scrolling effect as the typing happens 
    letter-spacing: 0.15em; Adjust as needed 
    white-space: nowrap;
    max-width: 100%;
    animation: 
      typing 3.5s steps(40, end),
      blink-caret 0.75s step-end infinite; */
  }


    /* The typing effect */
    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }

    /* The typewriter cursor effect
    @keyframes blink-caret {
      from, to { border-color: transparent }
      50% { border-color: plum; }
    } */
</style>

