<script setup>
defineProps({ blok: Object })
</script>

<template>
  <section v-editable="blok" class="bg-white dark:bg-gray-900">
    <div class="container px-6 py-10 mx-auto">
      <div class="text-center">
        <h1 class="text-2xl font-semibold text-gray-800 capitalize lg:text-3xl dark:text-white">{{ blok.title }}
        </h1>

        <p class="max-w-lg mx-auto mt-4 text-gray-500">
          {{ blok.description }}
        </p>
      </div>

      <div class="grid grid-cols-1 gap-8 mt-8 lg:grid-cols-2">
        <Article v-for="(post, index) in blok.posts" :post="post" :key="index" />
      </div>
    </div>
  </section>
</template>