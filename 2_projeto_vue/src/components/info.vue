<template>
    <div>

        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else >Estou procurando emprego.</p>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul >
            <!-- Diretivas de repeticao, por exemplo, devem ser colocadas dentro das tags que serao
            Realmente repetidas, no caso abaixo ira repetir as linhas LI e nao a Tabela UL.-->
            <li v-for="(tecnology, index) in backend_technologies" v-bind:key="index">{{ tecnology }}</li>        
        </ul>
        
        <p>Utilizo as seguintes linguagens de front-end</p>
        <ul >
            <!-- Diretivas de repeticao, por exemplo, devem ser colocadas dentro das tags que serao
            Realmente repetidas, no caso abaixo ira repetir as linhas LI e nao a Tabela UL.-->
            <li v-for="tecnology in frontend_technologies" :key="tecnology.id">{{ tecnology.language }}</li>        
        </ul>

        <div>
            <button @click="showEmail">{{ textoBotaoEmail }}</button>    
        </div>
        <p v-show="mostrar_email">Mande um email para: {{ email }} </p>
        <p class="teste">Para acessar meu portfolio <a v-bind:href="meu_link" target="_blank"> Basta acessar esse link</a></p>
        <Picture />

    </div>
      
</template>

<script>
import Picture from './Picture.vue'

export default {
 
    name: 'Info',
    props: {
        email: String,
        esta_trabalhando: Boolean
    },
    components: {
        Picture 
            } ,
    data(){
        return {
           // esta_trabalhando: true,
            mostrar_email: false,
            //email: 'matheus@email.com',
            meu_link: 'https://www.google.com.br',
            textoBotaoEmail: 'Mostrar Email',
            backend_technologies: ['JavaScript', 'Php', 'python','Java'],
            frontend_technologies: [
            {id: 1, language: 'HTML'},
            {id: 2, language: 'CSS'},
            {id: 3, language: 'Vuejs'}
            ]
        }
    },
    methods: {
        showEmail(){
            this.mostrar_email = !this.mostrar_email;
            if (this.mostrar_email){
                this.textoBotaoEmail = 'Ocultar email'
            }else{
                this.textoBotaoEmail = 'Mostrar email'
            }
        }

    }
}
</script>

<style>
.paragrafo-pai{
    color: red;
}

ul{
    text-decoration: none;
    /*circulo da lista  */
    list-style: none;
}

a {
    color: #DDD;    
    text-decoration: none;
    transition: .5s;
  }

</style>