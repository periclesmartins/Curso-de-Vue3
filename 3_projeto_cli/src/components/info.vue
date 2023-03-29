<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Últilizo as seguintes tecnologias:</p>
    <ul>
        <li>Html</li>
        <li>Css</li>
        <li>Javascript</li>
    </ul>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
  </div>
</template>
<script>
export default {
  name: 'Info',
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: false,
      email: 'pericles@gmail.com'
    }
  }
}
</script>