<script setup>


function onlyRunOnEnter() {
  console.log("You Pressed Enter");
}

function onlyRunOnSpace() {
  console.log("You Pressed Space");
}

function detectKeyPress(event) {
  console.log("you pressed "+event.key)
}

function doSomething() {
  console.log("you clicked");
}

function submitForm() {
  console.log("you submit a form");
}

</script>

<template>

  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Events Vue.js</h1>
<!--    <form @submit.prevent action="https://google.com/search">-->
    <form @submit.prevent="submitForm()" action="https://google.com/search">
      <div>
<!--         <input @keypress="detectKeyPress($event)"  type="text" name="q" />-->
<!--         <input @keypress.space="onlyRunOnSpace()" @keypress.enter="onlyRunOnEnter()"  type="text" name="q" />-->
         <input  type="text" name="q" />
<!--         <input @keyup="detectKeyPress($event)"  type="text" name="q" />-->
<!--       <button @click="doSomething()" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">-->
<!--          Do Something-->
<!--        </button>-->

<!--       <input type="text" name="q" />&ndash;&gt;-->
<!--       <button @click="doSomething()" type="submit" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">-->
       <button type="submit" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
          Submit
       </button>

      </div>
    </form>
  </section>

</template>

<style scoped>

</style>