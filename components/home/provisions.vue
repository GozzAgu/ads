<template>
  <section class="relative w-full bg-white dark:bg-black py-20 transition-colors duration-300">
    <div class="max-w-7xl mx-auto px-6">
      <h2 class="text-xl md:text-4xl font-extrabold text-gray-800 dark:text-gray-200 mb-5 border-l-4 border-red-500 dark:border-red-600 pl-4">
        Discover Visioni & Strauss
      </h2>
      <p class="text-gray-700 dark:text-gray-300 text-xs md:text-sm">
        Visioni & Strauss is a dynamic, private indigenous company proudly based in Nigeria.
        Fully registered with the Corporate Affairs Commission (CAC) in July 2007 (Registration Number 698755), 
        we bring a unique blend of multidisciplinary expertise to the table spanning Oil & Gas, Infrastructure, 
        Renewable Energy, and Civil Engineering. Our legacy is built on delivering exceptional 
        quality and integrated solutions to Government bodies, corporate entities, and individual clients alike.
      </p>

      <div class="mt-12 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
        <div v-for="(card, index) in cards" :key="index"
          class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-md transform transition-transform hover:scale-105 hover:shadow-lg">
          <h3 :class="card.color" class="text-xl font-bold text-center">
            {{ card.title }}
          </h3>
          <p class="text-center mt-3 text-gray-600 dark:text-gray-300 text-xs md:text-sm">
            {{ card.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const cards = ref([
  { title: "Net Zero", description: "Our ambition for 2050, in alignment with global sustainability goals.", color: "text-green-600 dark:text-green-400" },
  { title: "100,000", description: "Innovators and contributors across 120+ countries.", color: "text-blue-600 dark:text-blue-400" },
  { title: "100 Years", description: "Of collective vision, ideas, and relentless drive.", color: "text-red-900" }
]);
</script>

<style scoped>
.card {
  @apply bg-white rounded-md font-semibold dark:bg-zinc-900 shadow-md p-8 border-b-2 transition-transform hover:scale-105;
}
.card:nth-child(1) {
  @apply border-green-400 dark:border-green-500;
}
.card:nth-child(2) {
  @apply border-blue-500 dark:border-blue-600;
}
.card:nth-child(3) {
  @apply border-red-900;
}

.card:hover {
  @apply border-b-4;
}
</style>