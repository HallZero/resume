<template>
    <main>
        <div class="image">
            <img id="profile-picture" src="/img/Filipi.jpeg" alt="Filipi's picture">
        </div>
        <div class="text">
            <h1>Filipi Enzo Siqueira Kikuchi</h1>

            <div class="subinfo">
                <h2>He/Him</h2>
                <h2>07/02/2003</h2>
            </div>
            
            <div class="subinfo">
                <div>
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
                </div>

                <div>
                    <h3>Languages</h3>
                    <div>
                        <img class="flag" src="/img/brazil.png" alt="Portuguese">
                        <img class="flag" src="/img/usa.png" alt="English">
                        <img class="flag" src="/img/japan.png" alt="Japanese">
                    </div>
                </div>
            </div>
            
        </div>
    </main>

</template>

<script setup>

</script>

<style scoped>
    main {
        display: grid;
        align-items: center;
        grid-template-columns: 1fr 1fr;
        column-gap: 5px;
    }

    .text{
        border: 2px solid #222;
        padding: 0 auto;
        justify-content: center;
        align-items: center;
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

    .image{
        margin: 0 50px;
    }

    .subinfo{
        display: grid;
        grid-template-columns: 1fr 1fr;
    }

    .subinfo h2{
        display: inline;
        margin-right: 10px;
    }
</style>