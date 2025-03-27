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
        <div class="card">
          <h3 class="text-green-600 dark:text-green-400 text-2xl">Net Zero</h3>
          <p class="mt-2 text-gray-600 dark:text-gray-300 text-xs md:text-sm">Our ambition for 2050, in alignment with global sustainability goals.</p>
        </div>
        <div class="card">
          <h3 class="text-blue-600 dark:text-blue-400 text-2xl">100,000</h3>
          <p class="mt-2 text-gray-600 dark:text-gray-300 text-xs md:text-sm">Innovators and contributors across 120+ countries.</p>
        </div>
        <div class="card">
          <h3 class="text-red-900 text-2xl">100 Years</h3>
          <p class="mt-2 text-gray-600 dark:text-gray-300 text-xs md:text-sm">Of collective vision, ideas, and relentless drive.</p>
        </div>
      </div>
    </div>
  </section>
</template>

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