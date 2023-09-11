
<template>
    <img :src="avatar" :alt="descricao">
    <MudarImagem @trocar-imagem="trocarImagem"/>
</template>

<script>

import MudarImagem from './MudarImagem.vue';

export default {

    name: 'Draw',
    components:{

        MudarImagem
    },
    data() {

        return {
            avatar: "/assets/avatar.png",
            descricao: 'Renato'
        }
    },
    methods:{
          
        trocarImagem(){

            this.avatar = '/assets/logo.png',
            this.descricao = 'outra pessoa'
        }
    }
}
</script>