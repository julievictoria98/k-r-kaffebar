<template>
  <div class="content text-media">
    <div>
      <h2>{{ title }}</h2>
      <p class="mt-1">{{ text }}</p>
      <div class="mt-4">
        <UiPrimaryButton
          text="LÆS MERE OM DETTE"
          href="/contact"
        ></UiPrimaryButton>
      </div>
    </div>
    <div class="grid grid-cols-5 max-h-[400px] h-full">
      <div class="image-wrapper h-full col-start-1 col-span-3">
        <img
          src="../public/images/brunch-plate.png"
          alt="brunch"
          class="w-full h-full object-cover"
        />
      </div>
      <div class="image-wrapper-2 col-start-3 col-end-6 h-full">
        <img
          src="../public/images/brunch-plate.png"
          alt="brunch"
          class="w-full h-full object-cover"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
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
