<template>
  <h1>Meu nome é {{ nome }}</h1>
  <Info :email="email" :esta_trabalhando=false />
</template>

<script>
import Info from './Info.vue'

export default {
  name: 'LifeCycle',
  components: {
    Info
  },
  data() {
    return { 
      nome: "Ainda não sei",
      email: "matheus@gmail.com"
    }
  },
  created() {
    this.nome = "Matheus"
  }
}
</script>