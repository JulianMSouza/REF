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
    </div>
      
</template>

<script>
export default {
    name: 'Info',
    data(){
        return {
            esta_trabalhando: true,
            mostrar_email: true,
            email: 'matheus@email.com'
        }
    }
}
</script>