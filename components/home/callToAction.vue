<template>
  <section class="relative w-full py-16 bg-zinc-950 flex items-center justify-center">
    <div class="cta-container">
      <h2 class="text-3xl md:text-5xl font-bold text-gray-200 text-center">
        Let's Build Something Amazing Together
      </h2>
      <p class="text-lg text-gray-400 text-center mt-4">
        Join us in shaping the future with innovative solutions tailored for success.
      </p>
      <div class="mt-6 flex justify-center">
        <NuxtLink to="/contact" class="cta-button">Get Started</NuxtLink>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cta-container {
  @apply backdrop-blur-lg rounded-xl p-8 md:p-12 max-w-7xl shadow-lg transition-all duration-300;
  text-align: center;
}

.cta-button {
  @apply bg-red-900 text-white font-semibold px-6 py-3 rounded-lg text-lg 
    shadow-md hover:scale-105 transition-transform duration-300;
}
</style>