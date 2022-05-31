<template>
    <img :src="avatar" :alt="descricao">
</template>

<script>
export default {
    name: "UserPicture",
    data() {
        return {
            avatar: "/img/usericon.jpg",
            descricao: "Nome do Usuário"
        }
    }
}
</script>