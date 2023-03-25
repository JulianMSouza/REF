<template>
    <div>
        <Reutilizacao />
        <h1>Ola Vue!!</h1>
        <Reutilizacao />
        <p>Meu nome eh  {{  nome }} e trabalho como {{ profissao }}</p>
        <MultiplosEventos />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
    </div>
   
</template>

<script>

import MultiplosEventos from './MultiplosEventos.vue';

import Reutilizacao from './Reutilizacao.vue';

    export default {
        name: 'Primeiro Componente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return {
                nome: "Matheus",
                profissao: "Programador"
            }
        }
    }
</script>