<template>
    <div class="info">
        <p v-if="esta_trabalhando"> estou trabalhando no momento.</p>
        <p v-else>estou em busca de novas oportunidades.</p>

        <h3>Linguagens/talentos</h3>
        <ul>
            <li v-bind:key="index" v-for="(tecnologias, index) in frontend_technologies">{{ tecnologias }}</li>
        </ul>
        <div>
            <button @click="ShowEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para reisvierarenato@gmail.com</p>
        <Draw />
    </div>
</template>

<script>

import Draw from './Picture.vue';

export default {

    name: 'Info',
    components: {
        Draw
    },
    data() {

        return {

            mostrar_email: false,
            url_portifolio: "https://github.com/euRenatoReis",
            textoBotao: "Mostrar Email",
            frontend_technologies: [
                'Html',
                'Css',
                'Javascript',
                'React.js',
                'Vue.js',
                'Sei passar Café'
            ]
        }
    },props:{
        email: String,
        esta_trabalhando: Boolean
    },
    methods: {

        ShowEmail() {
            this.mostrar_email = !this.mostrar_email
            if (!this.mostrar_email) {

                this.textoBotao = "Mostrar Email"
            } else {

                this.textoBotao = "Esconder Email"
            }
        }
    }
}
</script>

<style scoped>
button {

    display: flex;
    border-radius: 15px;
    width: 190px;
    height: 30px;
    justify-content: center;
    align-items: center;
    border: none;
    box-shadow: -4px 15px 49px 19px rgb(124, 201, 118);
    background-color: rgba(153, 214, 149, 1);
    color: rgb(2, 78, 12);
}

button:hover {

    box-shadow: -4px 15px 49px 19px rgba(153, 214, 149, 1);
    color: white;
}
</style>
 