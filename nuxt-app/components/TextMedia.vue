<template>
  <div class="content">
    <h2>{{ title }}</h2>
    <p>{{ text }}</p>
    <a :href="buttonLink">
      <button>{{ buttonText }}</button>
    </a>
  </div>
</template>

<script setup>
// Define props properly with type and default values
const props = defineProps({
  title: {
    type: String,
    default: "Default Title",
  },
  text: {
    type: String,
    default: "Default Text",
  },
  buttonText: {
    type: String,
    default: "Default Button Text",
  },
  buttonLink: {
    type: String,
    default: "#",
  },
});
</script>
