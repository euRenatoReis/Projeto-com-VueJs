<template>
    <h1>meu formulario:</h1>
    <form action="" @submit="enviarFormulario($event)">
        <div>
            <input type="text" v-model="name">
        </div>
        <div>
            <input type="text" v-model="email">
        </div>
        <div>
            <input type="submit">
        </div>
    </form>
</template>

<script>

export default {

    name: 'Form',
    data() {

        return {
            name: 'Renato Vieira',
            email: 'reisvierarenato@gmail.com'
        }
    },
    methods: {

        enviarFormulario(e) {

            e.preventDefault()

            const name = this.name;
            const email = this.email;

            console.log('enviado');
            console.log('o nome é: ', name);
            console.log('o email é: ', email)
        }
    }
}


</script>