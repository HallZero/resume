<template>
    <main>
        <div class="image">
            <img id="profile-picture" src="/img/Filipi.jpeg" alt="Filipi's picture">
        </div>
        <div class="text">
            <h1>Filipi Enzo Siqueira Kikuchi</h1>
            <h2>He/Him | 07/02/2003</h2>
            <h3>Contacts:</h3>
            <ul>
                <li>
                    Email: filipikikuchi@gmail.com
                </li>
                <li>
                    Linkedin: Filipi linkedin
                </li>
                <li>
                    Github: HallZero
                </li>
            </ul>
            <h3>Education: Computer Engeneer @ Inteli</h3>
            <div>
                <h3>Languages</h3>
                <div>
                    <img class="flag" src="/img/brazil.png" alt="Portuguese">
                    <img class="flag" src="/img/usa.png" alt="English">
                    <img class="flag" src="/img/japan.png" alt="Japanese">
                </div>
            </div>
        </div>
    </main>

</template>

<script setup>

</script>

<style scoped>
    main {
        border: 2px solid #222;
        display: grid;
        align-items: center;
        grid-template-columns: 1fr 1fr;
        column-gap: 5px;
    }

    .container{
        display: grid;
        align-items: center;
        grid-template-columns: 1fr 1fr;
        column-gap: 5px;
    }

    #profile-picture{
        border-radius: 50%;
    }

    .flag{
        height: 30px;
        width: 30px;
        margin: 2px;
    }
</style>