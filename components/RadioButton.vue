<script setup lang="ts">
import { ref } from 'vue'

export interface Choice {
  id: string
  label: string
}

export interface Props {
  choices: Choice[]
  question: string
}

const props = defineProps<Props>()

const choices = ref(props.choices)
const question = ref(props.question)
</script>

<style scoped>
.quiz {
  --color-primary: #FF5700;
}
</style>

<template>
  <fieldset>
    <legend>{{ question }}</legend>

    <div v-for="(choice, index) in choices" :key="choice.id">
      <input type="radio" id="{{ choice.id }}" name="author" value="{{ choice.label }}">
      <label for="{{ choice.id }}">{{ choice.label }}</label>
    </div>
  </fieldset>
</template>

<!-- <style>
fieldset {
  border: 0.25rem solid #ccc;
  border-radius: 0.5rem;
  padding: 0.5em 1em;
}
</style> -->
