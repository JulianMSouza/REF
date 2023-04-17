<template>
    
    <div id="nav">
        <router-link to="/" id="logo_url">
            <img :src="logo" :alt="alt" id="logo">
        </router-link>
    <router-link to="/">Home</router-link> |
    <router-link to="/pedidos">Pedidos</router-link>
    </div>

</template>

<script>

export default{
    name: "Navbar",
    props: ["logo", "alt"]
}

</script>

<style scoped>
#nav{
    background-color: #222;
    border-bottom: 4px solid #111;
    padding: 15px 50px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

/* Posicao principal do campo imagem   */
#nav #logo_url{
    margin: auto;
    margin-left: 0;
}

/* Posicao do logo da imagem   */
#logo{
    width: 40px;
    height: 40px;
}

/* Estilo do link  */
#nav a{
    color: #FCBA03;
    text-decoration: none;
    margin: 12px;
    transition: .5s;

}

/* Animacao do link  */
#nav a:hover{
    color: #FFF;

}

</style>