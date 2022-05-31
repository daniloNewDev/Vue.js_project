<template>
    <h1>Meu nome é: {{ nome }}.</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return{
            nome: "Não sei ainda"
        }
    },
    created() {
        setTimeout(()=>{
            this.nome = "Moshe"
        }, 1000);
        this.lifeCycle()
    },
    mounted() {
        setTimeout(()=>{
            this.nome = "Itzchak"
        }, 2000)
        
    },
    methods: {
        lifeCycle(){
            console.log("Executou")
        }
    }
}
</script>