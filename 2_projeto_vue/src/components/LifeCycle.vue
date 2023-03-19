<template>
    <h1>Meu nome eh {{ nome }} </h1>
</template>

<script>
export default{
    name: "LyfeCycle",
    data(){
        return{
            nome: "Ainda nao sei"
        }
    },
    created(){
        setTimeout(() => {
            this.nome = "Matheus"
        }, 1000)

       this.lifeCycle();
       console.log(`created`);
        
    }, 
    mounted(){  //Mounted tem por questao de hierarquia prioridade para sobreescrever o componente.
                //Em relacao ao created. 
        setTimeout(() => {
            this.nome = "Pedro"
        }, 2000)
       
        this.lifeCycle();
        //console.log(`mounted`);

    },
    methods: {
        lifeCycle(){
           // console.log(`executou`);
        }
    }
}

</script>