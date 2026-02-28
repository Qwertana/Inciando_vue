<template>
<div>
<p v-if="numero <0"> número negativo! </p>
<p v-if="numero >0"> número positivo! </p>
<h1>Número atual: {{numero}}</h1>
 <br><br> 
<button @click="numero++">Aumentar numero</button>
<button @click="numero--">Diminuir numero</button>
</div>
</template>

<script setup>
import { ref } from 'vue'

const numero = ref(0)

function aumentar() {
  numero.value++
}

function diminuir() {
  numero.value--
}
</script>
