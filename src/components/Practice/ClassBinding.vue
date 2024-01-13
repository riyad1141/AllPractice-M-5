<script setup>

const bgOrange = "bg-orange-400";
const bgIndigo = "bg-indigo-400";
const bgGreen = "bg-green-400";

const weekend = false;

const colors = {
  bgColor: "bg-teal-100",
  borderColor: "border-teal-500",
  textColor: "text-teal-900",
}

const messageType = "Success";

if (messageType === "Warning") {
  colors.bgColor = "bg-red-400";
  colors.borderColor = "bg-red-400";
  colors.textColor = "bg-red-400";
}



</script>

<template>

  <section class="container mx-auto">
    <h1 class="text-center text-3xl py-12">Class & Style blinding</h1>
    <section class="flex space-x-10">
      <div class="w-1/3 h-16"  :class="bgOrange"></div>
      <div class="w-1/3 h-16"  :class="bgIndigo"></div>
      <div class="w-1/3 h-16" :class="bgGreen"></div>
    </section>
  </section>

  <section class="mt-10">
    <!--    <div class=" h-16 flex items-center justify-center text-white" v-bind:class="Weekend? 'bg-red-600':'bg-green-600'">-->
<!--    <div class=" h-16 flex items-center justify-center text-white" v-bind:class="[weekend? 'bg-red-600':'bg-green-600', weekend===true? 'text-2xl':'text-4xl']">-->
    <div class=" h-16 flex items-center justify-center text-white" :class="[weekend === true? 'bg-red-600':'bg-green-600', weekend === true? 'text-2xl':'text-4xl']">
      It's a weekDay
    </div>
  </section>


  <section class="mt-10">
    <div class=" border-t-4 rounded-b px-4 py-3 shadow-md" role="alert" v-bind:class="[colors.bgColor, colors.borderColor, colors.textColor]">
      <!--    <div class=" border-t-4 rounded-b px-4 py-3 shadow-md" role="alert">-->
      <p class="font-bold">Our Privacy Policy has Changed</p>
      <p class="text-sm">Make sure you know how these changes affect you</p>
    </div>
  </section>


</template>

<style scoped>

</style>