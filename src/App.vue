<script setup>
import { ref } from 'vue'

const diferente = ref(false)
const igual = ref(false)
const matriz1 = [
  [5, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
]
const matriz2 = [
  [1, 2, 3],
  [4, 5, 6],
  [3, 6, 7]
]

function compara() {
  if (
    matriz1[0].length == matriz2[0].length &&
    matriz1[1].length == matriz2[1].length &&
    matriz1[2].length == matriz2[2].length
  ) {
    for (let i = 0; i < matriz1[0].length; i++) {
      for (let j = 0; j < matriz2.length; j++) {
        if (matriz1[i][j] !== matriz2[i][j]) return false, alert('São diferentes')
      }
      return true, alert('São iguais')
    }
  }
} 
</script>

<template>
  <div>
    <button @click="compara()">claudio</button>
    <div class="igual" v-if="compara">MATRIZES IGUAIS</div>
    <div class="diferente" v-else-if="compara = false">MATRIZES DIFERENTES</div>
    <div v-else>PRIMEIRO COMPARE AS MATRIZES</div>
  </div>
</template>
