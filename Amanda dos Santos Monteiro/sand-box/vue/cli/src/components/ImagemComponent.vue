<template>
    <div class="container">
        <img v-show="imagemVisivel" :src="pathImagem" :alt="banner">
             <button @click="apareceEsconde(), segundoMetodo()">Aparece/Esconde</button>
    </div>
</template>

<script>
    export default {
        name: "ImagemComponent",
        data() {
            return {
                imagemVisivel : true,
                banner: "valor do alt",
                pathImagem : "https://static.poder360.com.br/2024/09/Vasco-Viva-Sorte-848x477.jpg"
            }
        },
        methods: {
            apareceEsconde(){
                this.imagemVisivel = !this.imagemVisivel; 
            },
            segundoMetodo(){
                setTimeout(() => {
                    alert('Segundo Método Acionado')
                }, 2000);
            }
        }
     }
</script>

<style>

    img{
        width: 300px;
        height: auto;
        border: solid 4px darkcyan;
        margin: 16px;
        border-radius: 16px;
        box-shadow: 2px 2px 10px 2px darkcyan;
    }

    button {
        padding: 12px;
        font-weight: bold;
        color: darkcyan;
        background: azure;
        border: solid 2px darkcyan;
        border-radius: 8px;
        cursor: pointer;
        transition: 0.5s;
    }

    button:hover {
        background-color: darkcyan;
        color: azure;
    }

    .container {
        display: flex;
        flex-direction: column;
        width: 50%;
        align-items: center;
        margin: 16px;
        border-bottom: solid 2px lightblue;
        padding: 16px;

    }

</style>