<script setup>
const { blok } = defineProps({ blok: Object })
</script>

<template>
  <div v-if="blok.spotlight" v-editable="blok" class="w-full p-8 space-y-8 text-center bg-blue-600 rounded-lg">
    <p class="font-medium text-gray-200 uppercase">{{ blok.title }}</p>

    <h2 class="text-5xl font-bold text-white uppercase dark:text-gray-100">
    {{ blok.price }}
    </h2>

    <p class="font-medium text-gray-200">{{ blok.duration }}</p>

    <button
      class="w-full px-4 py-2 mt-10 tracking-wide text-blue-500 capitalize transition-colors duration-300 transform bg-white rounded-md hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:ring focus:ring-gray-200 focus:ring-opacity-80">
    {{ blok.buttonText }}
    </button>
  </div>

  <div v-editable="blok" v-else
    class="w-full p-8 space-y-8 text-center border border-gray-200 rounded-lg dark:border-gray-700">
    <p class="font-medium text-gray-500 uppercase dark:text-gray-300">{{blok.title}}</p>

    <h2 class="text-4xl font-semibold text-gray-800 uppercase dark:text-gray-100">
      {{ blok.price }}
    </h2>

    <p class="font-medium text-gray-500 dark:text-gray-300">{{ blok.duration }}</p>

    <button
      class="w-full px-4 py-2 mt-10 tracking-wide text-white capitalize transition-colors duration-300 transform bg-blue-600 rounded-md hover:bg-blue-500 focus:outline-none focus:bg-blue-500 focus:ring focus:ring-blue-300 focus:ring-opacity-80">
      {{ blok.buttonText }}
    </button>
  </div>
</template>   