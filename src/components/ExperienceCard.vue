<template>
    <div class="container">
        <img src="/img/Filipi.jpeg" alt="Experience Photo">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illum inventore dolorum accusantium at temporibus pariatur doloremque praesentium recusandae sed aspernatur magnam suscipit earum quo saepe nobis consequatur, perspiciatis fuga totam.</p>
        <button>
            Learn More
        </button>
    </div>
</template>

<script>
    export default{
        name: "ExperienceCard"
    }
</script>

<style scoped>
    .container{
        border: 2px solid #222;
        border-radius: 5%;
        margin: 15px;
        width: 400px;
        height: 650px;
        align-items: center;
        display: flex;
        flex-direction: column;
        text-align: center;
        justify-content: center;
    }

    .container img{
        border: 2px solid #222;
        width: 300px;
        height: 300px;
        margin: 0 auto;
    }


</style>