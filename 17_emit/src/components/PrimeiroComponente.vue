<template>
  <h1>Olá Vue!</h1>
  <MultiplosEventos />
  <div>
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
  </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'
export default {
  components: { MultiplosEventos, Reutilizacao },
  name: 'PrimeiroComponente',
}
</script>