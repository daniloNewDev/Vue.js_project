<template>
    <p v-if="esta_trabalhando">Estou trabalhando atualmente.</p>
    <p v-else>Estou em busca de novas oportunidades.</p>
    <p>Utiliza as tecnologias: </p>
    <ul>
        <li>JavaScript</li>
        <li>Node.js</li>
        <li>Vue.js</li>
    </ul>
    <div><button @click="showEmail">Mostrar e-mail</button></div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a>.</p>
    <Picture />
</template>

<script>
import Picture from './Picture.vue'
export default {
    name: "UserInfo",
    components:{
        Picture
    },
    data(){
        return {
            esta_trabalhando: false,
            mostrar_email: false,
            email: "danilo@email.com",
            meu_link: 'https://google.com'
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
        }
    }
}
</script>