<template>
    <div>
        <PrimeiroComponente   />   <!-- teg de vue para componentes-->
        <p>O dado de App eh {{ testando }}</p>
    </div>
   
</template>

<script>

import PrimeiroComponente from './components/PrimeiroComponente.vue'
export default {
    name:  'App',
    components: {
        PrimeiroComponente
    },
    data(){
        return {
            testando: "Teste"
        }
    }
}
    


</script>