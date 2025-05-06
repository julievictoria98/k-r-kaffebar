<template>
  <div>
    <div
      @click="toggleAccordion"
      :class="accordionClass"
      class="accordion-header"
    >
      <h2>{{ props.question }}</h2>
      <img src="../../public/images/brown-arrow.svg" alt="brown arrow" />
    </div>
    <p v-if="isOpen">
      {{ props.answer }}
    </p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

// Linter-friendly: no destructuring
const props = defineProps<{
  question: string
  answer: string
}>()

const isOpen = ref(false)

const toggleAccordion = () => {
  isOpen.value = !isOpen.value
}

const accordionClass = computed(() => {
  return isOpen.value ? 'accordion-open' : 'accordion-closed'
})
</script>

<style scoped>
.accordion-header {
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em;
  border: 1px solid #ccc;
  transition: background-color 0.3s ease;
}

.accordion-open {
  background-color: #f0f0f0;
}

.accordion-closed {
  background-color: #ffffff;
}

p {
  padding: 1em;
  margin: 0;
  border: 1px solid #ccc;
  border-top: none;
}
</style>
