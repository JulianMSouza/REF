<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else >Estou procurando emprego.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>Javascript</li>
            <li>PHP</li>
            <li>Html</li>
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
    components: {
        Picture 
            } ,
    data(){
        return {
            esta_trabalhando: true,
            mostrar_email: false,
            email: 'matheus@email.com',
            meu_link: 'https://www.google.com.br',
            textoBotaoEmail: 'Mostrar Email'
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

</style>