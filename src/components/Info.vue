<template>
    <p v-if="esta_trabalhando">Estou trabalhando atualmente.</p>
    <p v-else>Estou em busca de novas oportunidades.</p>
    <p>Utiliza as tecnologias: </p>
    <ul>
        <li v-for="(technology, index) in backend_technologies" v-bind:key="index">{{ technology }}</li>
    </ul>
    <p>Utilizo a seguintes tecnologias para Front-end</p>
    <ul>
        <li v-for="technology in frontend_technologies" :key="technology.id">
            {{ technology.language }}
        </li>
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
    props: {
        email: String,
        esta_trabalhando: Boolean,
    },
    data(){
        return {
            mostrar_email: false,
            meu_link: 'https://google.com',
            backend_technologies: ["Node.js", "PHP", "Python"],
            frontend_technologies: [
                {id: 1, language: "HTML"},
                {id: 2, language: "CSS"},
                {id: 3, language: "Vue.js"}
                ]
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
        }
    }
}
</script>