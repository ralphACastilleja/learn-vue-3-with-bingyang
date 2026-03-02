<template>
  <div class="card">
    <h2>Message: {{ message }}</h2>
    <h2>Number: {{ number }}</h2>
    <button @click="changeMessageToUpperCase">Change message to upper case</button>
    <button @click="incrementNumber">Increment number</button>
  </div>
<div class = "card">
  <h2>Name: {{ wizard.name }}</h2>
    <h2>Wand: {{ wizard.wand }}</h2>
    <button @click="changeNameToUpperCase">Change name to upper case</button>
    <button @click="changeWandCore">Change wand core to upper case</button>
    <button @click="changeWizard">Change wizard</button>


</div>
<div class = "card">
  <h2>Array:{{ wizards }}</h2>
  <button @click="wizards.push('Draco')">Add Wizard</button>
</div>

</template>

<script setup>
import { ref } from 'vue'
let message = ref('Hello, Reactivity!')
let number = ref(1)

function changeMessageToUpperCase() {
  message.value = message.value.toUpperCase()
  console.log(message)
}

function incrementNumber() {
  number.value += 1
  console.log(number)
}

let wizard = ref({
  id: 1001,
  name: 'Harry Potter',
  house: 'Gryffindor',
  age: 17,
  wand:{
    core: 'Phoenix Feather',
    wood: 'Holly',
  }
})


function changeNameToUpperCase() {
  wizard.value.name = wizard.value.name.toUpperCase()
  console.log(wizard)
}

function changeWandCore() {
  wizard.value.wand.core = 'Unicorn Hair'
}

function changeWizard() {
  wizard.value = {
    id: 1002,
    name: 'Hermione Granger',
    house: 'Gryffindor',
    age: 17,
    wand:{
      core: 'Dragon Heartstring',
      wood: 'Vine',
    }
  }
}

let wizards = ref((['Harry', 'Hermione', 'Ron',]))

</script>

<style scoped>
.card {
  border: 1px solid purple;
}
</style>