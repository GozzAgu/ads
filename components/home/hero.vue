<template>
  <section class="relative w-full h-screen flex items-center justify-center text-white">
    <div class="absolute inset-0">
      <img src="" alt="Energy Future" class="w-full h-full object-cover hidden lg:block">
      <div class="absolute inset-0 bg-black/50"></div>
    </div>

    <div class="relative text-center px-6 z-10 max-w-3xl">
      <h1 class="text-4xl md:text-6xl font-bold uppercase leading-tight">
        Shaping a Sustainable Future
      </h1>
      <p class="mt-4 text-lg md:text-xl text-gray-200">
        Discover how we innovate to create cleaner energy solutions for a better tomorrow.
      </p>
      <div class="mt-6">
        <NuxtLink to="/about" class="cta-button">Learn More</NuxtLink>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cta-button {
  @apply bg-red-600 hover:bg-red-700 text-white px-6 py-3 rounded-full text-lg font-semibold transition-all duration-300;
}
</style>