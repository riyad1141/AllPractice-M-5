<script setup>

const bgOrange = "background-color: rgba(251,146,60, 1)";
const bgIndigo = "background-color: rgba(129,140,248,1)";
const bgGreen = "background-color: rgba(52,211,153,1)";


const bgRed = "background-color: rgba(220,38,38,1)";
const bgDarkGreen = "background-color: rgba(5,150,105,1)";

const colors = {
  borderColor: 'rgba(20,184,166,1)',
  color: 'rgba(19,78,74,1)',
  backgroundColor: 'rgba(204,251,241,1)'
}

const weekday = false;


const messageType = "success";

if (messageType === "error"){
  borderColor =  'rgba(239,68,68,1)';
  color = 'rgba(254,226,226,1)';
  backgroundColor = 'rgba(127,29,29,1)';
}


</script>

<template>

  <section class="container mx-auto">
    <h1 class="text-center text-3xl py-12">Class & Style blinding</h1>
    <section class="flex space-x-10">
      <div class="w-1/3 h-16"  :style="bgOrange"></div>
      <div class="w-1/3 h-16"  :style="bgIndigo"></div>
      <div class="w-1/3 h-16" :style="bgGreen"></div>
    </section>
  </section>

  <section class="mt-10">
    <div class=" h-16 flex items-center justify-center text-white" :style="[weekday === true? bgRed:bgDarkGreen, weekday===true?'font-size:20px':'font-size:30px']">
      It's a weekDay
    </div>
  </section>


  <section class="mt-10">
    <div class=" border-t-4 rounded-b px-4 py-3 shadow-md" role="alert" :style="colors">
      <p class="font-bold">Our Privacy Policy has Changed</p>
      <p class="text-sm">Make sure you know how these changes affect you</p>
    </div>
  </section>


</template>

<style scoped>

</style>