<template>
    <h2>Meu formulario</h2>
    <form action="">
        <div>
            <InputText />       
        </div>
        <div>
            <InputText />       
        </div><div>
            <submit />      
        </div>

        
    </form>
</template>

<script>
import InputText from './form/inputText.vue'
import Submit from './form/submit.vue'

    export default{
        name: 'form',
        components: {
            InputText,
            Submit  
        }
    }
</script>
