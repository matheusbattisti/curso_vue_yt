<template>
  <div>
    <Header />
    <PrimeiroComponente />
    <LifeCycle />
  </div>
</template>

<script>
import Header from './components/Header'
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    Header
  }
}
</script>

<style>
  body {
    background-color: #333;
    color: #FFF;
  }
</style>