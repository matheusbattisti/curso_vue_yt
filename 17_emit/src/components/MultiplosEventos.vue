<template>
  <button @click="primeiro($event), segundo($event)">Ativar múltiplos eventos</button>
  <p>{{ multiplos_eventos }}</p>
</template>
<script>

export default {
  name: 'MultiplosEventos',
  components: {

  },
  data() {
    return {
      multiplos_eventos: ""
    }
  },
  methods: {
    primeiro() {
      this.multiplos_eventos = "Primeiro evento"
    },
    segundo() {
      setTimeout(() => this.multiplos_eventos = "Segundo evento", 500)
    }
  }
}
</script>