<template>
    <h1>Shalom, chaver Vue!</h1>
    <p>Meu nome é {{ nome }}. Vou trabalhar como {{ profissao }}.</p>
</template>

<script>
export default {
    name: "PrimeiroComponente",
    data() {
        return {
            nome: "Danilo",
            profissao: "Dev"
        }
    }
}
</script>