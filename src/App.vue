<template>
<h1>message: {{ message }}</h1>
<hr />
<h1>number: {{ number }}</h1>
<hr />

<h1>doubleNum(50): {{ doubleNum(50) }}</h1>
<hr />
<h1>number * 2 = {{ number * 2 }}</h1>
<hr>
<h1> {{ number > 150? 'number is greater then 150':'number is less then 150' }}</h1>
<hr/>
<h1 v-text="number"></h1>
<hr/>
<h1> {{ harry }}</h1>
<h1> {{ harry.name}}</h1>
<hr1>{{ hogwartsWizards }}</hr1>
<hr1>{{ hogwartsWizards[0] }}</hr1>
<hr/>
<h1>{{ rawHrml }}</h1>
<h1 v-text="rawHrml"></h1>






</template>

<script setup>
let message  = 'hello, Vue!'
let number = 50

function doubleNum(num){
   return num * 2
}

let harry = {
  id: 1001,
  name: 'Harry Potter',
  house: 'Gryffindor',
  age: 17,
  wand: {
    core: 'Phoenix feather',
    wood: 'Holly'
  }
}



const hogwartsWizards = [
  {
    id: 1001,
    name: 'Harry Potter',
    house: 'Gryffindor',
    age: 17,
    wand: {
      core: 'Phoenix feather',
      wood: 'Holly'
    }
  },
  {
    id: 1002,
    name: 'Hermione Granger',
    house: 'Gryffindor',
    age: 17,
    wand: {
      core: 'Dragon heartstring',
      wood: 'Vine'
    }
  },
  {
    id: 1003,
    name: 'Ron Weasley',
    house: 'Gryffindor',
    age: 17,
    wand: {
      core: 'Unicorn hair',
      wood: 'Willow'
    }
  },
  {
    id: 1004,
    name: 'Draco Malfoy',
    house: 'Slytherin',
    age: 17,
    wand: {
      core: 'Dragon heartstring',
      wood: 'Hawthorn'
    }
  }
];

let rawHrml = '<span style="color:red">This should be red.</span>'

</script>




<style lang="scss" scoped></style>