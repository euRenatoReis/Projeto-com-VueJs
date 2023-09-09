
<template>
    <img :src="avatar" :alt="descricao">
    
</template>

<script>

    export default{

        name: 'Draw',
        data(){

            return{
                avatar: "./assets/avatar.png",
                descricao: 'Renato'
            }
        }
    }
</script>