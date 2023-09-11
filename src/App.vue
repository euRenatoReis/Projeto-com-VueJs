
<template>
      <Cabecalho />
      <Candidato />
      <Formulario />
      <Reutilizacao/>
</template>


<script>

import Cabecalho from './components/Cabecalho.vue';
import Candidato from './components/Candidato.vue';
import Formulario from './components/Formulario.vue';
import Reutilizacao from './components/Reutilizacao.vue';

export default {

      name: "App",
      components: {

            Cabecalho,
            Candidato,
            Formulario,
            Reutilizacao
      }
}

</script>

<style>
body {
      background-color: #494949;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 20px;

}

.candidato {

      display: flex;
      justify-content: center;
      flex-direction: column;
      padding: 20px;
      border-radius: 20px;
      border: solid 1px white;
      background-color: rgb(75, 105, 73);
      box-shadow: -4px 15px 49px 19px rgb(74, 126, 71);
}

.info {

      display: flex;
      gap: 20px;
      flex-direction: column;
      background-color: darkslategrey;
      padding: 20px;
      border-radius: 20px;
      border: solid 1px white;
      justify-content: center;
      box-shadow: -4px 15px 49px 19px rgb(115, 175, 111);
}
</style>
