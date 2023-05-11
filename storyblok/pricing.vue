<script setup>
  const {blok} = defineProps({blok: Object})
</script>

<template>
  <div v-editable="blok" class="bg-white dark:bg-gray-900">
    <div class="container px-6 py-8 mx-auto">
        <h1 class="text-2xl font-semibold text-center text-gray-800 capitalize lg:text-3xl dark:text-white">{{ blok.title }}</h1>

        <div v-html="renderRichText(blok.richtext)" class="max-w-2xl mx-auto mt-4 text-center text-gray-500 xl:mt-6 dark:text-gray-300">
            
        </div>

        <div class="grid grid-cols-1 gap-8 mt-6 xl:mt-12 xl:gap-12 md:grid-cols-2 lg:grid-cols-3">
           <StoryblokComponent v-for="(item, index) in blok.body" :key="index" :blok="item"/>
        </div>
    </div>
</div>
</template>