<script setup>

import { ref } from "vue"

const space = ref(0)
const pressed = ref("nothing")


function sayHi(){
  alert("Hi")
}

function clicked(){
  alert("Clicked")
}

const divClicked = () => {
  alert("Div Clicked")
}

const buttonClicked = () => {
  alert("Button Clicked")
}

</script>

<template>

  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Events Vue.js</h1>
    <h2 class="mt-10">{{ message }}</h2>
    <form @submit.prevent action="https://google.com/search">
      <div class="container mx-auto flex space-x-5 justify-center m-5">
        <input @keypress.space="space++" type="text"  class="border border-gray-500 bg-white p-5"  placeholder="Press Space">
      </div>

      <p>Space pressed {{ space }} <span v-text="space<=1?'time':'times'"></span></p>
      <!-- <p>Space pressed {{ space }} <span v-if="space<=1">time</span><span v-else>times</span></p> -->

      <div class="container mx-auto flex space-x-5 justify-center m-5">
        <input @keyup="pressed=$event.key" name="text" type="text" class="border border-gray-500 bg-white p-5"  placeholder="Type Something">
      </div>

      <p>You pressed {{ pressed }}</p>

      <button @click.once="sayHi()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" >
        Button
      </button>

      <button @click.shift="clicked()" class="mt-5 bg-blue-500 ml-5 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" >
        Shift + Click
      </button>

    </form>

    <div @click="divClicked()" class="bg-gray-200 w-[500px] h-80 mt-5 flex items-center justify-center"  >
      <button @click.stop="buttonClicked()" class="bg-orange-500 hover:bg-orange-700 text-white font-bold py-2 px-4 rounded"  >
        Button
      </button>
    </div>
  </section>

</template>

<style scoped>

</style>