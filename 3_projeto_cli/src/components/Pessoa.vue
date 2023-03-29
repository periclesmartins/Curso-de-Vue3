<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        <Info />
        <Form />
    </div>
</template>
<script>
import Info from './Info'
import Form from './Form'
export default {
    nome: 'Pessoa',
    components: {
        Info,
        Form
    },
    data() {
        return {
            nome: 'Calmo, Dedicado, Resiliente.'
        }
    }
}
</script>