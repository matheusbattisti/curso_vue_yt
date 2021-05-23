<template>
  <img :src="avatar" :alt="descricao">
  <MudarImagem @mudar-imagem="mudarImagem" />
</template>
<script>
import MudarImagem from './MudarImagem.vue'

export default {
  components: { MudarImagem },
  name: 'Picture',
  data() {
    return { 
      avatar: "/img/avatar.png",
      descricao: "Matheus Battisti"
    }
  },
  methods: {
    mudarImagem() {
      this.avatar = "/img/avatar2.png"
    }
  }
}
</script>