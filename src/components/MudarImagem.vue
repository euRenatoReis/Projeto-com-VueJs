<template>
    <div>
        <button @click="$emit('trocarImagem')">
            Trocar a imagem
        </button>
    </div>
</template>

<script>

export default {

  name: 'BotaoMudarImagem', 
  emits: ['trocarImagem']

}

</script>