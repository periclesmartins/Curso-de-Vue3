<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        
    </div>
</template>
<script>
export default {
    nome: 'Pessoa',
    data() {
        return {
            nome: 'Péricles'
        }
    }
}
</script>