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
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p>Para acessar meu portfólio <a v-bind:href="meu_link" target="blank">basta clicar aqui!</a></p>
    <Picture />
  </div>
</template>
<script>
import Picture from './Picture.vue'
export default {
  name: 'Info',
  components: {
    Picture
  },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: false,
      email: 'pericles@gmail.com',
      meu_link: 'https://google.com.br',
      textoBotao: 'Mostrar e-mail'
    }
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
      if (!this.mostrar_email) {
        this.textoBotao = 'Mostrar e-mail'
      } else {
        this.textoBotao = 'Esconder e-mail'
      }
    }
  }
}
</script>