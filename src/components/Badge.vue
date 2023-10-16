<template>
    <div class="container">
        <img :src="src" :alt="alt">
        <ProgressBar />
    </div>
</template>

<script>
    import ProgressBar from './ProgressBar.vue';

    export default{
        name: 'Badge',
        components: {
            ProgressBar
        },
        props: ["src", "alt"]
    }
</script>

<style scoped>
    .container{
        border: 2px dashed #000;
        border-radius: 10%;
        width: 300px;
        height: 400px;
        align-items: center;
        justify-content: center;
        display: flex;
        flex-direction: column;
        margin: 10px;
    }

    img{
        width: 100px;
    }
</style>