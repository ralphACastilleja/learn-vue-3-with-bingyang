<template>
    <div>
      <div>
        Press down the "Enter" key will trigger a console log print:
        <input type="text" @keydown.enter="logKey('Enter')">
      </div>
  
      <div>
        Press down the "Arrow Down" key will trigger a console log print:
        <input type="text" @keydown.down="logKey('Arrow Down')">
      </div>
  
      <div>
        Press down the "Space" key will trigger a console log print:
        <input type="text" @keydown.space="logKey('Space')">
      </div>
  
      <div>
        Press down the "b" key will trigger a console log print:
        <input type="text" @keydown.b="logKey('b')">
      </div>

      <div>
        Press down the "ctrl + c " key will trigger a console log print:
        <input type="text" @keydown.ctrl.c="logKey('ctrl + c')">
      </div>

    </div>
  <h1>{{ message }}</h1>

  <button v-on:click="replaceText('v-on is fun!')">Replace text</button>
  <button @click="replaceText('v-on is fun!')">Replace text</button>
  <hr/>
  <p> An input field where the user can only input numbers:</p>
  <input type="text" @keydown="handleInput($event)">



  
<hr/>
<div style ="width: 100px; height: 100px; background-color: lightblue" @contextmenu.prevent="console.log('Show a custom context menu')">
  </div>
  <div id="mouseover" @mouseover="fun1">
    <textarea @mouseover.stop="fun2($event)">This is text area</textarea>"
  </div>"


  
</template>

<script setup>
import { ref } from 'vue'

let message = ref('Hello, v-on!')

function replaceText(msg) {
  message.value = msg
}
function handleInput(event) {
  console.log(event)
let keyCode = event.keyCode
if (keyCode < 48 || keyCode > 57) {
  event.preventDefault()
  }
}

function fun1() {
  console.log('Mouse is over the div')
}

function fun2(event) {
  //event.stopPropagation()
  console.log('Mouse is over the textarea')
}



</script>


<style scoped>
#mouseover {
  margin: 100px;
  text-align: right;
  background-color: purple;
  width: 300px;
  height: 300px;
}



</style>