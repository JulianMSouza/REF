<template>
    <div>
    <h2>Meu formulario</h2>
    
        <form action="" @submit="enviarFormulario($event)">
            <div>
                <input  type="text" v-model="name" >
            </div>
            <div>
                <input  type="text" v-model="email" >
   
            </div>
            <div>
                <submit />      
            </div>
        </form>
        <p>Conteudo</p>
        <p>Conteudo</p>
        <p>Conteudo</p>
    </div>
</template>

<script>
import InputText from './form/inputText.vue'
import Submit from './form/submit.vue'

    export default{
        name: 'form',
        components: {
            InputText,
            Submit  
        },
        data() {
            return{
                name:"",
                email: ""
            }
        },
        methods: {
            enviarFormulario(e) {
            e.preventDefault();

            const name = this.name;
            const email =  this.email;

            console.log('O nome eh ' + name);
            console.log('O email eh ' + email);


            }
        }
    }
</script>

<style scoped>

p {
    margin: 150px;
}

</style>