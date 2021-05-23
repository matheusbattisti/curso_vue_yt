<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p v-else>Estou em busca de novas oportunidades!</p>
  <p>Utilizo as seguintes tecnologias para back-end:</p>
  <ul v-bind:key="index" v-for="(technology, index) in backend_technologies">
    <li>{{ technology }}</li>
  </ul>
    <p>Utilizo as seguintes tecnologias para front-end:</p>
  <ul v-bind:key="index" v-for="(technology, index) in frontend_technologies">
    <li>{{ technology }}</li>
  </ul>
  <div>
    <button @click="showEmail">Mostrar e-mail</button>
  </div>
  <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
  <p>Para acessar meu portfólio <a v-bind:href="url_portfolio">basta clicar aqui</a></p>
  <Picture />
  <div>
    <button @click="primeiro($event), segundo($segundo)">Ativar múltiplos eventos</button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>
<script>
import Picture from './Picture'

export default {
  name: 'Info',
  components: {
    Picture
  },
  props: {
    email: String,
    esta_trabalhando: Boolean
  },
  data() {
    return {
      mostrar_email: false,
      url_portfolio: "https://www.google.com",
      backend_technologies: ["JavaScript", "PHP", "Python"],
      frontend_technologies: ["HTML", "CSS", "Vue"],
      multiplos_eventos: ""
    }
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
    },
    primeiro() {
      this.multiplos_eventos = "Primeiro evento"
    },
    segundo() {
      setTimeout(function() {
        this.multiplos_eventos = "Segundo evento"
      }, 300);
    }
  }
}
</script>