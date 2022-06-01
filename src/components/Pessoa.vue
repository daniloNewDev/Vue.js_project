<template>
    <h2>A descrição da Pessoa é: {{ nome }}</h2>
    <Info :email="email" :esta_trabalhando=false />
    <Form />
</template>

<script>
import Info from './Info'
import Form from './Form'
export default {
  components: { Info, Form },
    name: 'UserPessoa',
    data() {
        return {
            nome: "Avraham",
            email: "danilo2@email.com"
        }
    }
}
</script>