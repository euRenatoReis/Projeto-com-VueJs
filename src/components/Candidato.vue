
<template>
    <div class="candidato">
        <h3>Meu nome é: {{ nome }}</h3>
        <Info :email="email" :esta_trabalhando="true"/>
        <MultiplosEventos/>
        <Reutilizacao/>
    </div>
</template>

<script>

import Info from './Info.vue';
import MultiplosEventos from './MultiplosEventos.vue';
import Reutilizacao from './Reutilizacao.vue';

export default {

    name: 'Candidato',
    components: {
        Info,
        MultiplosEventos,
        Reutilizacao
    },
    data() {

        return {

            nome: 'ainda não sei...'
        }
    },
    created() {

        this.nome = "Renato Vieira"
    },
}

</script>

<style>

   h3{
    
     color:  rgba(153,214,149,1);
     z-index: 3;
   }

</style>