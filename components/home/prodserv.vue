<script setup>
const activeTab = ref('power');

const isPowerTab = computed(() => activeTab.value === 'power');
const isEnergyTab = computed(() => activeTab.value === 'energy');
</script>

<template>
  <section class="bg-zinc-100 dark:bg-zinc-900 py-5 md:py-20 px-6">
    <div class="max-w-7xl mx-auto md:px-6">
      <h2 class="text-xl md:text-4xl font-extrabold text-gray-800 dark:text-gray-200 mb-5 border-l-4 border-red-500 dark:border-red-600 pl-4">Products & Services</h2>
      <div class="flex border-b border-gray-300 dark:border-gray-700">
        <button 
          class="tab-button" 
          :class="{ active: isPowerTab }" 
          @click="activeTab = 'power'"
        >
          ⚡ Keeping You Powered
        </button>
        <button 
          class="tab-button" 
          :class="{ active: isEnergyTab }" 
          @click="activeTab = 'energy'"
        >
          🌱 Smart Energy Stops
        </button>
      </div>

      <div class="mt-12 grid md:grid-cols-3 gap-6">
        <div v-if="isPowerTab" class="card">
          <img src="https://images.unsplash.com/photo-1605647257485-28019bfed0e8?q=80&w=3540&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="EV Charging" class="card-img">
          <div class="p-4 md:p-6">
            <h3 class="card-title flex items-center gap-2">
              Smart Charging Stations
            </h3>
            <p class="card-text">Discover our fast-charging network for electric vehicles.</p>
            <a href="#" class="card-link">Learn about Visionee Charge</a>
          </div>
        </div>
        <div v-if="isPowerTab" class="card">
          <img src="https://images.unsplash.com/photo-1582377224944-2c2a17affa38?q=80&w=3542&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Energy Solutions" class="card-img">
          <div class="p-4 md:p-6">
            <h3 class="card-title flex items-center gap-2">
              Sustainable Fuels
            </h3>
            <p class="card-text">Explore our range of clean and efficient energy sources.</p>
            <a href="#" class="card-link">See our Fuel Innovations</a>
          </div>
        </div>
        <div v-if="isPowerTab" class="card">
          <img src="https://images.unsplash.com/photo-1520433259178-0a6b180165fa?q=80&w=3540&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Battery Solutions" class="card-img">
          <div class="p-4 md:p-6">
            <h3 class="card-title flex items-center gap-2">
              Battery Tech for the Future
            </h3>
            <p class="card-text">Find the best energy storage solutions for your needs.</p>
            <a href="#" class="card-link">Discover our Battery Tech</a>
          </div>
        </div>

        <div v-if="isEnergyTab" class="card">
          <img src="https://images.unsplash.com/photo-1613665813446-82a78c468a1d?q=80&w=3516&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Solar Energy" class="card-img">
          <div class="p-4 md:p-6">
            <h3 class="card-title flex items-center gap-2">
              Solar Power Solutions
            </h3>
            <p class="card-text">Harness the sun’s energy with our solar tech.</p>
            <a href="#" class="card-link">Explore Solar Innovations</a>
          </div>
        </div>
        <div v-if="isEnergyTab" class="card">
          <img src="https://images.unsplash.com/photo-1548337138-e87d889cc369?q=80&w=3592&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Wind Energy" class="card-img">
          <div class="p-4 md:p-6">
            <h3 class="card-title flex items-center gap-2">
              Wind Energy Advancements
            </h3>
            <p class="card-text">Discover how we harness wind for sustainable energy.</p>
            <a href="#" class="card-link">See Our Wind Solutions</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.tab-button {
  @apply text-gray-700 dark:text-gray-300 text-xs md:text-sm font-semibold px-2 py-1 border-b-4 border-transparent transition-all;
}
.tab-button.active {
  @apply border-gray-500 text-gray-500 dark:text-gray-200;
}

.card {
  @apply bg-white rounded-md dark:bg-black overflow-hidden shadow-sm transition-transform duration-200 ease-out;
  will-change: transform;
}
.card:hover {
  @apply scale-[1.02] shadow-lg;
}

.card-img {
  @apply w-full h-56 object-cover;
}
.card-title {
  @apply text-lg md:text-xl font-semibold text-gray-900 dark:text-gray-100 flex items-center gap-2;
}
.card-text {
  @apply text-xs md:text-base text-gray-600 dark:text-gray-300 mt-2 text-sm leading-relaxed;
}
.card-link {
  @apply text-xs md:text-base text-blue-600 dark:text-blue-400 font-semibold mt-4 inline-flex items-center gap-2 transition-all;
}
.card-link::after {
  content: " →";
  transition: transform 150ms ease-out;
}
.card-link:hover::after {
  transform: translateX(4px);
}

.tab-button.active {
  @apply border-gray-500 text-gray-500 dark:text-gray-200 dark:border-gray-500;
}
</style>