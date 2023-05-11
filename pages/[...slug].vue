<script setup>
const route = useRoute()
const { slug } = route.params

const story = await useAsyncStoryblok(
  slug && slug.length > 0 ? slug.join('/') : 'home',
  { version: 'draft' , resolve_relations:['blog.posts']},{
    resolveRelations:['blog.posts']
  }
)

</script>

<template>
  <StoryblokComponent v-if="story" :blok="story.content" />
</template>