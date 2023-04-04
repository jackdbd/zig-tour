<script setup lang="ts">
import { ref } from 'vue'

export interface Props {
  answers: string | number | boolean[]
  question: string
}

const props = defineProps<Props>()

const answers = ref(props.answers)
const question = ref(props.question)
</script>

<style scoped>
.quiz fieldset {
  border: 0.25rem solid var(--color-accent);
  border-radius: 0.5rem;
  padding: 0.5em 1em;
}

.quiz legend {
  font-weight: 700;  /* 700 = bold */
  padding: 0 0.5em;
}

.quiz label {
  margin-left: 0.5em;
}
</style>

<template>
  <div class="quiz stack">
    <fieldset>
      <legend><slot name="question">Question here</slot></legend>
      <div v-for="(answer, index) in answers">
        <input type="radio" :name="`answer-${index}`" :value="answer">
        <label :for="`answer-${index}`">{{ answer }}</label>
      </div>
    </fieldset>
    <slot name="extra"></slot>
  </div>
</template>
