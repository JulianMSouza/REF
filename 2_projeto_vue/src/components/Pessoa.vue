<template>
    <div>
        <h2>Essa eh a descricao da pessoa: {{ nome }}</h2>
        <Info />
    </div>

</template>

<script>

//Componente info esta no mesmo nivel do componente Pessoa, nesse caso nao necessita o ./components.
import Info from './info.vue'

export default  {
    name: 'Pessoa',
    components:{
        Info    
    },
    data(){
        return{
            nome: 'Matheus'
        }
    }
}
</script>