<script setup>
const matriz1 = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
]
const matriz2 = [
  [1, 2, 3],
  [4, 5, 6],
  [3, 6, 7]
]
console.log(matriz1[0])

function compara() {
  
  if (matriz1.length == matriz2.length) {
   
    for(let a of matriz1[i]){
      for(let b of matriz2[i]){ 
        if(a === b){console.log('elemento igaul')}
      }
    }
 
  }
  else alert('As matrizes sao diferentes')
}

function passamatriz(){
  let i = 0
  for (i = 0; i < 2; i++) {
    
  }
}
</script>

<template>
  <div>
    <button @click="compara()">claudio</button>
  </div>
</template>
