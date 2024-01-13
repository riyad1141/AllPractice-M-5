<script setup>
import {reactive} from "vue";

// const Location  = ref("Dhaka");

const location = reactive({
  name: "Dhaka",
  weather: "sunny"
});

function changeLocation(newLocation) {
  location.name = newLocation;
}


</script>

<template>

  <section class="container mx-auto items-center flex flex-col">
    <h1 class="text-center text-2xl py-10">Events and Reactive in Vue js</h1>
    <div class="container mx-auto justify-center space-x-5 m-5">
      <button @click="changeLocation('Dhaka')" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Dhaka
      </button>
      <button @click="changeLocation('USA')" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        USA
      </button>
      <h1 class="text-2xl m-10">{{location.name}}</h1>
    </div>
  </section>

</template>

<style scoped>

</style>