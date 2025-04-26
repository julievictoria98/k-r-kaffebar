<template>
  <article class="content">
    <div
      id="hero"
      class="h-screen flex items-center justify-center backdrop-blur-md col-span-full no-padding"
    >
      <div class="text-center">
        <h1 class="display">Welcome to Our Website</h1>
        <NuxtLink
          to="/contact"
          class="bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700 transition duration-300"
          >Get Started</NuxtLink
        >
      </div>
      <SecondaryCTA />
    </div>
  </article>
</template>
