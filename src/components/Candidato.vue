
<template>
    <div class="candidato">
        <h3>Meu nome é: {{ nome }}</h3>
        <Info />
    </div>
</template>

<script>

import Info from './Info.vue';

export default {

    name: 'Candidato',
    components: {
        Info
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