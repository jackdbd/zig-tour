<script setup lang="ts">
import Anchor from './Anchor.vue'

export interface Props {
  author?: string
  citeHref?: string
  citeText?: string
  text: string
}

const props = withDefaults(defineProps<Props>(), {
    text: 'Quote text'
})
</script>

<style scoped>
blockquote {
  /* background: linear-gradient(to right, var(--color-gray-light) 0%, var(--color-alabaster) 100%); */
  background: linear-gradient(to right, var(--color-alabaster) 0%, var(--color-gray-light) 100%);
  border: 0;
}

.quote {
  font-style: italic;
}
.quote::before {
  content: '“';
}
.quote::after {
  content: '”';
}

.author {
  font-style: normal;
}
</style>

<template>
  <blockquote :cite="citeHref">
    <p class="quote">{{ text }}</p>
    <p v-if="author" class="author">—{{ author }}</p>
    <footer v-if="citeHref && citeText" class="important-mt-2">Source: <Anchor :href="`${citeHref}`" :text="`${citeText}`" /></footer>
  </blockquote>
</template>
