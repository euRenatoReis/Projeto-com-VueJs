
<template>
    <div>
        <button @click="ativar"></button>
        <p v-show="ativou">ativou!</p>
    </div>
</template>


<script>
export default {
     name: 'Reutilizacao',
     data(){

        return{
            ativou: false
        }
     },
     methods: {
        ativar(){
           this.ativou = true
        }
     }    

}
</script>