<template>
    <img :src="avatar" :alt="descricao">
    <MudarImagem @mudar-imagem="trocarImagem" />
</template>

<script>
import MudarImagem from './MudarImagem.vue'
export default {
    name: "UserPicture",
    components: {
        MudarImagem
    },
    data() {
        return {
            avatar: "/img/usericon.jpg",
            descricao: "Nome do Usuário"
        }
    },
    methods: {
        trocarImagem() {
            this.avatar = "/img/user2.jpg"
        }
    }
}
</script>