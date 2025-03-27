<template>
  <section class="relative w-full pt-16 pb-32 dark:bg-black text-gray-300 dark:text-gray-200">
    <div class="max-w-7xl mx-auto px-6">
      <h2 class="text-xl md:text-4xl font-extrabold text-gray-700 dark:text-gray-200 mb-5 border-l-4 border-red-500 dark:border-red-600 pl-4">
        Meet Our Team
      </h2>
      <h4 class="text-xs md:text-lg text-gray-600 dark:text-gray-200 mb-4 tracking-wide">
        Passionate professionals dedicated to excellence.
      </h4>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-3 md:grid-cols-6 gap-8 p-6 max-w-7xl mx-auto mt-12">
      <div v-for="(member, index) in teamMembers" :key="index" class="team-card">
        <img :src="member.image" :alt="member.name" class="w-28 h-28 rounded-full">
        <h3 class="text-xs md:text-sm font-semibold mt-4 text-gray-600 dark:text-gray-100">{{ member.name }}</h3>
        <p class="text-xs text-gray-400 dark:text-gray-300">{{ member.role }}</p>
        <div class="flex space-x-4 mt-4">
          <a v-if="member.linkedin" :href="member.linkedin" target="_blank" class="icon">
            <Icon name="mdi:linkedin" class="text-blue-400 dark:text-blue-300 text-2xl" />
          </a>
          <a v-if="member.twitter" :href="member.twitter" target="_blank" class="icon">
            <Icon name="mdi:twitter" class="text-blue-300 dark:text-blue-400 text-2xl" />
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const teamMembers = [
  {
    name: "John Doe",
    role: "CEO & Founder",
    image: "https://randomuser.me/api/portraits/men/32.jpg",
  },
  {
    name: "Jane Smith",
    role: "CTO",
    image: "https://randomuser.me/api/portraits/women/44.jpg",
  },
  {
    name: "David Johnson",
    role: "Lead Developer",
    image: "https://randomuser.me/api/portraits/men/27.jpg",
  },
  {
    name: "John Doe",
    role: "CEO & Founder",
    image: "https://randomuser.me/api/portraits/men/32.jpg",
  },
  {
    name: "Jane Smith",
    role: "CTO",
    image: "https://randomuser.me/api/portraits/women/44.jpg",
  },
  {
    name: "David Johnson",
    role: "Lead Developer",
    image: "https://randomuser.me/api/portraits/men/27.jpg",
  }
];
</script>

<style scoped>
.team-card {
  @apply flex flex-col items-center p-6 rounded-lg transition-transform duration-300;
  backdrop-filter: blur(10px);
}

.icon {
  @apply p-2 rounded-full bg-gray-800 hover:bg-gray-700 dark:bg-gray-600 dark:hover:bg-gray-500 transition-all;
}
</style>