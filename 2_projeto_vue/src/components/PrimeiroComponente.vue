<template>
    <div>
        <h1>Ola Vue!!</h1>
        <p>Meu nome eh  {{  nome }} e trabalho como {{ profissao }}</p>
    </div>
   
</template>

<script>
    export default {
        name: 'Primeiro Componente',
        data(){
            return {
                nome: "Matheus",
                profissao: "Programador"
            }
        }
    }
</script>