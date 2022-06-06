<template>
    <header>

        <nav class="container">
        
         <a href="/"><img id="logo" src="../images/logodanti.png"></a>

        
        <img @click="openMenu"  id="menu" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg" alt="menu">

        <div @click="closeMenu" id="menu-overlay" v-if="menuActive"></div>

        <div id="menu-items" :class="{active:menuActive}">

            <img id="menu-logo" src="../images/logodanti.png" alt="Foto logo">

            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/videos">Vídeos</a></li>
                <li><a href="/sobre">Sobre</a></li>
                <li><a href="./ContatoOne.vue">Contato</a></li>
            
            </ul>

        </div>
        </nav>
    
    </header>
</template>

<script>
export default {
    name: 'HeaderOne',
    data () {
        return {
            menuActive: false
        }
    },
    methods: {
        openMenu: function() {
            this.menuActive=true;
        },
        closeMenu: function() {
            this.menuActive=false;
        }
    }
}


</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@500&display=swap');
    header {
        background-color: var(--color-background-nav);
        width: 100%;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    nav {
        display: flex;
        justify-content: space-between;
        height: 60px;
        align-items: center;
    }

    #logo {
        width:130px;
    }

    #menu {
        width:30px;
    }

    #menu-overlay {
        position: fixed;
        top:0px;
        left:0px;
        width: 40%;
        height:100vh;
        background-color: black;
        opacity: 0.8;
    }

    #menu-logo {
        width:110px;
        margin-top:30px;
        margin-bottom:10px;

    }

    #menu-items {
        position:fixed;
        top:0px;
        right:0px;
        background-color: var(--color-background-nav);
        font-family: 'Open Sans';
        font-weight: bold;
        width: 60%;
        height: 100vh;
        display: none;
        flex-direction: column;
        justify-content: flex-start;
        align-items:center;
    }

    #menu-items.active {
        display: flex;
    }

    ul {
        list-style: none;
        text-align: center
    }

    ul > li {
        margin: 20px 0px;
    }

    ul > li > a {
        color:var(--color-text-light);
    }

    @media (min-width: 700px) {
        #menu, #menu-logo, #menu-overlay {
            display: none;
        }

        #menu-items {
            display:flex;
            position: static;
            height: 60px;
            width: auto;
        }

        ul {
            display: flex;
            height: 60px;
            align-items: center;
        }

        ul li {
            margin: 0px;
            margin-left: 20px;
        }
    }
    
</style>