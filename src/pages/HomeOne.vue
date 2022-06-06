<template>
    
    <main>

    <div class="text-top">Acesse meu repositório no GitHub</div>

    <a href="https://github.com/AbraoDaniel" target="_blank">
        <img id="sub" src="../images/githublogo.png" alt="Acesse e Vá para meu gitHub" >
    </a>

    <div class="text-bottom">Projeto desenvolvido através dos ensinamentos de Wdev</div>
    
    </main>
</template>

<script>
    export default {
        name: 'HomeOne',
    }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@500&display=swap');

    main {
        background-color: var(--color-background-home);
        justify-content: center;
        align-items: center;
    }

    .text-top {
        color: var(--color-text-dark);
        font-size: 22px;
        font-family: 'Open Sans';
        font-weight: bold;
        margin-bottom: 20px;
    }

    #sub {
        width: 350px;
    }
    .text-bottom {
        color: var(--color-text-dark);
        font-size: 18px;
        font-family: 'Open Sans';
        font-weight: bold;
        margin-top: 20px;
    }

    @media (min-width: 700px) {
        #sub {
            width: 370px;
        }
    }

</style>