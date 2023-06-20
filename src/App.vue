<script setup>
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
    <div class="matrizes">
      <div class="matriz1">
        <h2>Matriz 1: </h2>
        <p>{{ matriz1[0] }}</p>
        <p>{{ matriz1[1] }}</p>
        <p>{{ matriz1[2] }}</p>
      </div>
      <img src="https://i.pinimg.com/564x/78/46/a8/7846a88f8efa7f880b5b9abea3f02a30.jpg" alt="">
      <div class="matriz2">
        <h2>Matriz 2: </h2>
        <p>{{ matriz2[0] }}</p>
        <p>{{ matriz2[1] }}</p>
        <p>{{ matriz2[2] }}</p>      
      </div>
    </div>
    <button @click="compara()">claudio</button>

</template>

<style scoped>
  .matrizes{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    font-family: Arial;
    font-size: large;
  }
  .matriz1{
    background-color: black;
    color: white;
    border-radius: 15px;
    width: 200px;
    height: 200px;
    padding: 10px;
    box-shadow: 3px 3px 5px gray;
  }
  .matriz2{
    background-color: black;
    color: white;
    border-radius: 15px;
    width: 200px;
    height: 200px;
    padding: 10px;
    box-shadow: 3px 3px 5px gray;
  }
  button{
    display: flex;
    margin: 10px auto;
    padding: 10px;
    border-radius: 15px;
    color: white;
    background-color: black;
    border: 1px solid black;
    font-size: larger;
    box-shadow: 3px 3px 5px gray;
  }
  button:hover{
    background-color: rgb(66, 66, 66);
  }
  img{

    border-radius: 15px;
  }
</style>