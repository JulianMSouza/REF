<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else >Estou procurando emprego.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ui>
            <li>Javascript</li>
            <li>PHP</li>
            <li>Html</li>
        </ui>
        <p v-show="mostrar_email">Mande um email para: {{ email }} </p>
        <p>Para acessar meu portfolio <a v-bind:href="meu_link" target="_blank"> Basta acessar esse link</a></p>
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
            mostrar_email: true,
            email: 'matheus@email.com',
            meu_link: 'https://www.google.com.br'
        }
    }
}
</script>