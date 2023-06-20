<script setup>
import { ref } from 'vue'

//const diferente = ref(false)
//const igual = ref(false)
const matriz1 = [
  [1, 2, 3],
  [4, 5, 6],
  [3, 6, 7]
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
    for (let posPai = 0; posPai < matriz1.length; posPai++) {
      let filho1 = matriz1[posPai];
      let filho2 = matriz2[posPai];
      for (let posFilho = 0; posFilho < filho1.length; posFilho++) {
        if (filho1[posFilho] != filho2[posFilho]) {
          alert('São diferentes!');
          alert(`Matriz 1, linha ${posPai+1}, ${posFilho+1}º elemento, valor: ${filho1[posFilho]}.`);
          alert(`Matriz 2, linha ${posPai+1}, ${posFilho+1}º elemento, valor: ${filho2[posFilho]}.`);
          return false;
        } else alert('São iguais')
      }
    }
  }
} 
</script>

<template>
  <div>
    <button @click="compara()">claudio</button>
  </div>
</template>
