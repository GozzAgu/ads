<template>
  <section class="relative w-full h-screen flex items-center justify-center text-white">
    <div class="absolute inset-0">
      <Swiper
        :modules="[Autoplay, Navigation]"
        :slides-per-view="1"
        :loop="true"
        :autoplay="{ delay: 5000, disableOnInteraction: false }"
        class="w-full h-full"
      >
        <SwiperSlide v-for="(image, index) in images" :key="index" class="relative">
          <img :src="image" alt="Energy Future" class="w-full h-full object-cover">
          <div class="absolute inset-0 bg-gradient-to-b from-black/60 via-black/40 to-black/60"></div>
        </SwiperSlide>
      </Swiper>
    </div>

    <div class="relative text-center px-6 z-10 max-w-3xl">
      <h1 class="text-4xl md:text-6xl font-bold uppercase leading-tight animated-text">
        Shaping a Sustainable Future
      </h1>
      <p class="mt-4 text-lg md:text-xl text-gray-200 animated-text">
        Discover how we innovate to create cleaner energy solutions for a better tomorrow.
      </p>
      <div class="mt-6">
        <NuxtLink to="/about" class="cta-button">Learn More</NuxtLink>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Navigation } from "swiper/modules";
import "swiper/css";
import "swiper/css/navigation";

const images = [
  "https://images.unsplash.com/photo-1548337138-e87d889cc369?q=80&w=3592&auto=format&fit=crop",
  "https://images.unsplash.com/photo-1521747116042-5a810fda9664?q=80&w=3592&auto=format&fit=crop",
];
</script>

<style scoped>
.cta-button {
  @apply bg-red-900 rounded-md hover:bg-red-700 text-white px-6 py-3 text-lg font-semibold transition-all duration-300;
}

:deep(.swiper-button-next), :deep(.swiper-button-prev) {
  color: white;
  transition: opacity 0.3s;
}
:deep(.swiper-button-next:hover), :deep(.swiper-button-prev:hover) {
  opacity: 0.8;
}

/* Text Animation */
.animated-text {
  animation: fadeInUp 1s ease-out;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>