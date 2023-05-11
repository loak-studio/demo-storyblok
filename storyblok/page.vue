
 
<script setup>
const { blok } = defineProps({ blok: Object });
</script>
<template>
  <div class="layout">
      <StoryblokComponent v-for="blok in blok.body" :key="blok._uid" :blok="blok" />
  </div>
</template>
