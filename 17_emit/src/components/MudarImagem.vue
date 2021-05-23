<template>
  <div>
    <button @click="$emit('mudarImagem')">Trocar imagem de perfil</button>
  </div>
</template>
<script>
export default {
  name: 'MudarImagem',
  emits: ['mudarImagem']
}
</script>