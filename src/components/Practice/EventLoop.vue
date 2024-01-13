<script setup>

import {reactive, ref} from "vue";

const accordions = reactive([
  {
    heading: "What is term",
    content: "The accordion is a graphical control element comprising a vertically stacked list of items such as labels or thumbnails",
    isOpen: false,
  },
  {
    heading: "When to use according components",
    content: "The accordion is a graphical control element comprising a vertically stacked list of items such as labels or thumbnails",
    isOpen: false,
  },
  {
    heading: "How can it be defined",
    content: "The accordion is a graphical control element comprising a vertically stacked list of items such as labels or thumbnails",
    isOpen: false,
  },
  {
    heading: "Chamber reached do he nothing be",
    content: "The accordion is a graphical control element comprising a vertically stacked list of items such as labels or thumbnails",
    isOpen: false,
  }
]);

const activeIndex = ref(0);

</script>

<template>

  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Events & Reactivity in Vue.js</h1>

    <div class="w-full p-10 bg-gradient-to-br from-pink-50 to-indigo-100 grid place-items-center">
      <div class="w-3/4 mx-auto rounded border">
        <div class="bg-white p-10 shadow-sm">
          <h3 class="text-lg font-medium text-gray-800">Several Windows stacked on each other</h3>
          <p class="text-sm font-light text-gray-600 my-3">
            The accordion is a graphical control element comprising a vertically stacked list of items such as labels or thumbnails
          </p>

          <div class="h-1 w-full mx-auto border-b my-5"></div>

          <!-- What is term -->
          <div v-for="accordion in accordions" class="transition hover:bg-indigo-50">
            <!-- header -->
            <div @click="accordion.isOpen = !accordion.isOpen" class="accordion-header cursor-pointer transition flex space-x-5 px-5 items-center h-16">
              <i class="fas fa-plus"></i>
              <h3 class="bg-green-400">{{accordion.heading}}</h3>
            </div>
            <!-- Content -->
            <div  class="px-5 pt-0 text-left pb-5" v-show="accordion.isOpen" >
              <p class="leading-6 font-light bg-red-400 pl-9">
                {{accordion.content}}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>




  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Events & Reactivity in Vue.js</h1>

    <div class="w-full p-10 bg-gradient-to-br from-pink-50 to-indigo-100 grid place-items-center">
      <div class="w-3/4 mx-auto rounded border">
        <div class="bg-white p-10 shadow-sm">
          <h3 class="text-lg font-medium text-gray-800">Several Windows stacked on each other</h3>
          <p class="text-sm font-light text-gray-600 my-3">
            The accordion is a graphical control element comprising a vertically stacked list of items such as labels or thumbnails
          </p>

          <div class="h-1 w-full mx-auto border-b my-5"></div>

          <!-- What is term -->
          <div v-for="(accordion,index) in accordions" class="transition hover:bg-indigo-50">
            <!-- header -->
            <div @click="activeIndex = index" class="accordion-header cursor-pointer transition flex space-x-5 px-5 items-center h-16">
              <i class="fas fa-plus"></i>
              <h3 class="bg-green-400">{{accordion.heading}}</h3>
            </div>
            <!-- Content -->
            <div  class="px-5 pt-0 text-left pb-5" v-show="index === activeIndex" >
              <p class="leading-6 font-light bg-red-400 pl-9">
                {{accordion.content}}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

</template>

<style scoped>

</style>