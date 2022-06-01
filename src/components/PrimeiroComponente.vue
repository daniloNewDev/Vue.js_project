<template>
    <h1>Shalom, chaver Vue!</h1>
    <p>Meu nome é {{ nome }}. Vou trabalhar como {{ profissao }}.</p>
    <MultiplosEventos />
    <Reutilizacao />
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
import Reutilizacao from './Reutilizacao.vue';
export default {
    name: "PrimeiroComponente",
    components: {
        MultiplosEventos,
        Reutilizacao
    },
    data() {
        Reutilizacao
        return {
            nome: "Danilo",
            profissao: "Dev"
        }
    }
}
</script>