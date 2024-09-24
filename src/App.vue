<script setup>
import { ref } from 'vue';
import { reactive } from 'vue';

let gramsToEat = undefined;
let kmsToFly = undefined;

const pepita = reactice({
  energy: 0,
})

function displayGrams(){
  console.log(gramsToEat);
}

function displayKms(){
  console.log(kmsToFly)
}

function eat(){
pepita.energy += gramsToEat * 4;
console.log(pepita.energy)
}

function fly(){
  pepita.energy -= kmsToFly * 2 + 10;
  console.log(pepita.energy)
}
</script>


<template>
<h2 id=pepitaEnergy> Pepita's Energy: {{ pepita.energy }} </h2>
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS8pmzkiZrt6qzwXx0NY_-v6bCsEdF1sJ4pew&s"></img>

<input type="number" v-model="gramsToEat" placeholder="Grams">
<button @click='displayGrams'>Eat</button>

<input type="number" v-model="kmsToFly" placeholder="Kilometers">
<button @click='displayKms'>Fly</button>
</template>



<style scoped>
</style>