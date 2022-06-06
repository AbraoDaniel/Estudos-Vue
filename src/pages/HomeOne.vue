<template>
    
    <main>
        <div class="text-top">Acesse meu repositório no GitHub</div>
            <a href="https://github.com/AbraoDaniel" target="_blank">
            <img id="sub" src="../images/githublogo.png" alt="Acesse e Vá para meu gitHub" >
            </a>
        <div class="text-bottom">- Projeto desenvolvido através dos ensinamentos de Wdev -</div>

        <section class="container"> 
            
            <section class="contacts">

                <label id="labelcontact" for="contacts">Contatos</label>

                <div class="contact" v-for="(contact,index) in contacts" :key="index">
                    <div class="contact-title">{{ contact.title }} </div>
                    <a :href="contact.link" target="_blank">{{ contact.label }} </a>
                </div>
            
            </section>

        </section>
    
    </main>
</template>

<script>
    import api from '@/services/api.js';

    export default {
        name: 'HomeOne',
        data() {
            return {
                contacts: []
            }
        },
        mounted () {
            api.get('/contacts.json').then(response => {
                this.contacts = response.data;
            });
        }
    }
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@500&display=swap');

    main {
        background-color: var(--color-background-home);
        justify-content: center;
        align-items: center;
        font-family: 'Open Sans';
    }

    .container {
        display:flex;
        align-items: center;
        justify-content: center;
        
    }

    #labelcontact {
        font-size: 20px;
        font-family: 'Open Sans';
        font-weight: bold;
        text-align: center;
    }

    .contacts {
        margin-bottom: 40px;
        color: var(--color-text-dark);
        font-family:'Open Sans';
        text-align: center;
        
    }

    .contact-title {
        display:flex;
        font-weight: 600;
        font-size: 18px;
        
        
    }

    .contact a {
        color:var(--color-text-dark);
        font-family: 'Open Sans';
        
    }

    .contact {
        margin-bottom: 20px;
        margin-top: 20px;
        text-align: left;
    }


    .text-top {
        color: var(--color-text-dark);
        font-size: 18px;
        font-family: 'Open Sans';
        font-weight: bold;
        margin-top: 35px;
    } 
    
    #sub {
        width: 350px;
        display:flex;
    }
    
    .text-bottom {
        color: var(--color-text-dark);
        font-size: 16px;
        font-family: 'Open Sans';
        font-weight: bold;
        margin-top: 20px;
        margin-bottom: 20px;
    }

    @media (min-width: 700px) {
        #sub {
            width: 370px;
        }
    }
    
</style>