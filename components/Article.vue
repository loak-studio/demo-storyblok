<script setup>
defineProps({ post: Object })
</script>

<template>
  <div>
    <img class="relative z-10 object-cover w-full rounded-md h-96" :src="post.content?.image.filename" alt="">

    <div class="relative z-20 max-w-lg p-6 mx-auto -mt-20 bg-white rounded-md shadow dark:bg-gray-900">
      <a href="#" class="font-semibold text-gray-800 hover:underline dark:text-white md:text-xl">
        {{ post.content?.title }}
      </a>

      <p class="mt-3 text-sm text-gray-500 dark:text-gray-300 md:text-sm">
        {{ post.content?.description }}
      </p>

      <p class="mt-3 text-sm text-blue-500">{{ (new Date(post.content?.date)).toLocaleDateString('fr-FR', {
        day: '2-digit',
        month: 'long', year: 'numeric'
      }) }}</p>
    </div>
  </div>
</template>