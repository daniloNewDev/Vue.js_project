<template>
<h2>Meu Formulário: </h2>
    <form action="" @submit="enviarFormulario($event)">
        <div><input type="text" v-model="name"></div>
        <div><input type="text" v-model="email"></div>
        <div><Submit /></div>        
    </form>
</template>

<script>

import Submit from './form/Submit.vue'
export default {
    name: "UserForm",
    components: {
        Submit
    },
    data() {
        return {
            name: "",
            email: ""
        }
    },
    methods: {
        enviarFormulario(e) {

            e.preventDefault();

            const name = this.name;
            const email = this.email

            console.log("Enviado!")
            console.log("O nome é: " + name)
            console.log("O e-mail é: " + email)

            //  Ajax

            //  Inserir no banco os dados

        }
    }
}
</script>