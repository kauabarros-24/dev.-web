<script>
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() { 
      this.contador++
     },
     decrementarContador() {
      if (this.contador > 0) 
        this.contador--
     }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}`)
  }
}

</script>

<template>
  <button @click="incrementarContador">Incremetar</button>
  <button @click="decrementarContador">decrementar</button>
  <p>O valor do conteúdo é: {{ contador }}</p>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>