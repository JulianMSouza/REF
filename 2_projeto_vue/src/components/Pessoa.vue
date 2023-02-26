<template>
    <div>
        <h2>Essa eh a descricao da pessoa: {{ nome }}</h2>
        <Info />
        <Form />
    </div>

</template>

<script>

//Componente info esta no mesmo nivel do componente Pessoa, nesse caso nao necessita o ./components.
import Info from './info.vue'
import Form from './form.vue'



export default  {
    name: 'Pessoa',
    components:{
        Info,
        Form    
    },
    data(){
        return{
            nome: 'Matheus'
        }
    }
}
</script>