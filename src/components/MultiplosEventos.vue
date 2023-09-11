
<template>
    <div>
        <button @click="primeiro($event), segundo(txt2, $event), terceiro()">Ativar Multiplos Eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>


<script>
export default {

    name: 'MultiplosEventos',
    data() {

        return {
            multiplos_eventos: '',
            txt2: "segundo evento"
        }
    },
    methods: {

        primeiro(e) {
            this.multiplos_eventos = "primeiro evento ativado"
        },
        segundo(txt2, e) {
            setTimeout(() => this.multiplos_eventos = txt2, 500)
        },
        terceiro() {
            setTimeout(() => this.multiplos_eventos = "", 1000)
        }
    }

}
</script>

<style scoped>
div {
    margin: 100px;
}
</style>
