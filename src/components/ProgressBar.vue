<template>
    <div class="">
        <p>Level</p>
        <label for="">XP: </label>
        <progress id="experience" value="12" max="100"></progress>
    </div>
</template>

<script>
    export default{
        name: 'ProgressBar'
    }
</script>

<style scoped>
    .container{
        display: grid;
        margin: 5px;
    }
</style>