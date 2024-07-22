<script setup>
import { ref, onMounted } from 'vue';

const contador = ref(0);

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  if (contador.value == 0) 
    return
  contador.value--
}
function reiniciar() {
  if (contador.value != 0) {
    contador.value = 0
  }
}

onMounted(() => {
  console.log(`O valor do contador é ${contador.value}`)
})
</script>

<template>
  <button @click="incrementarContador">Incremetar</button>
  <button @click="decrementarContador">decrementar</button>
  <button @click="reiniciar">Reiniciar</button>

  <p>O valor do conteúdo é: {{ contador }}</p>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>