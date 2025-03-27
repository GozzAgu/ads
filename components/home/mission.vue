<template>
  <section class="relative w-full bg-zinc-200 dark:bg-zinc-950 py-12 md:py-20 transition-colors duration-300">
    <div class="max-w-7xl mx-auto px-6">
      <h2 class="text-xl md:text-4xl font-extrabold text-gray-700 dark:text-gray-200 mb-5 border-l-4 border-red-500 dark:border-red-600 pl-4">
        Our Vision & Mission
      </h2>
      <h4 class="text-lg text-gray-300 dark:text-gray-200 mb-4 tracking-wide">
        Leading the energy transition while prioritizing sustainability and innovation.
      </h4>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="info-card vision-card">
          <h3>Our Vision</h3>
          <p>
            We aspire to be the most preferred integrated solution partner by continuously building 
            on our experience and embracing innovation to drive sustainable progress.
          </p>
        </div>
        <div class="info-card mission-card">
          <h3>Our Mission</h3>
          <p>
            To leverage expertise and cutting-edge technology to deliver innovative, 
            sustainable, and high-quality solutions, ensuring every project sets a new standard.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.info-card {
  @apply p-8 rounded-lg backdrop-blur-md transition-transform duration-300 bg-white dark:bg-black;
}

h3 {
  @apply text-2xl font-bold mb-4 uppercase tracking-wide text-gray-700 dark:text-gray-400;
}

h4 {
  @apply text-lg mb-4 text-gray-700 dark:text-gray-400 tracking-wide;
}

p {
  @apply text-lg text-gray-700 dark:text-gray-400 leading-relaxed;
}

.info-card:hover {
  @apply scale-105 shadow-2xl;
}

.vision-card:hover {
  @apply border-green-400 dark:border-green-300;
}

.mission-card:hover {
  @apply border-blue-400 dark:border-blue-300;
}
</style>