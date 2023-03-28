<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Só sei que nada sei!'
        }
    },
    created() {
        setTimeout(() => {
            this.nome = 'Péricles'
        }, 1000)
    },
    mounted() {
        setTimeout(() => {
            this.nome = 'Péricles'
        }, 2000)
    }
}
</script>