<template>
  <section class="relative w-full pt-16 pb-32 dark:bg-black text-gray-300 dark:text-gray-200">
    <div class="max-w-7xl mx-auto px-6">
      <h2 class="text-xl md:text-4xl font-extrabold text-gray-700 dark:text-gray-200 mb-5 border-l-4 border-red-500 dark:border-red-600 pl-4">
        Meet Our Team
      </h2>
      <h4 class="text-xs md:text-lg text-gray-600 dark:text-gray-200 mb-4 tracking-wide">
        Board of Directors
      </h4>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-3 md:grid-cols-4 gap-8 p-6 max-w-7xl mx-auto mt-12">
      <div v-for="(member, index) in teamMembers" :key="'board-' + index" class="team-card">
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

    <div class="max-w-7xl mx-auto px-6 mt-16">
      <h4 class="text-xs md:text-lg text-gray-600 dark:text-gray-200 tracking-wide mb-6">Management Team</h4>
      <div class="grid grid-cols-1 gap-8">
        <div
          v-for="(member, index) in management"
          :key="'management-' + index"
          class="team-card relative"
        >
          <h3 class="text-xs md:text-sm font-semibold mt-2 text-gray-700 dark:text-white">
            {{ member.name }}
          </h3>

          <p
            class="text-xs text-gray-500 dark:text-gray-300 mt-2 transition-all duration-300 overflow-hidden"
            :class="{ 'line-clamp-2': activeIndex !== index }"
          >
            {{ member.role }}
          </p>

          <button
            @click="toggleExpanded(index)"
            class="mt-2 text-xs text-red-400 hover:underline focus:outline-none"
          >
            {{ activeIndex === index ? 'Show Less' : 'Read More' }}
          </button>

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
    </div>
  </section>
</template>

<script setup>
const teamMembers = [
  {
    name: "Mr. Obinna M. Ibe",
    role: "Executive Director",
  },
  {
    name: "Anita Ejiogu",
    role: "Executive Director",
  },
  {
    name: "Alhaji Shehu Sambo",
    role: "Executive Director",
  },
  {
    name: "Chief D. M. Ejogu",
    role: "Chief Executive Director",
  },
];

const management = [
  {
    name: "Engr. Opadere Ezekiel Segun",
    role: "An experienced professional in Building Technology, Engr. Opadere holds an HND from Kwara State Polytechnic, Ilorin. He is a registered member of the Nigeria Institute of Building and the Council of Registered Builders of Nigeria (CORBON). With years of hands-on experience, he has contributed to various high-impact construction and project management roles across Nigeri",
  },
  {
    name: "Engr. Omeni Macgerald Anejionu",
    role: "Engr. Omeni is a certified Civil Engineer with a B.Eng. degree and active memberships in both the Nigeria Society of Engineers (MNSE) and the Council for the Regulation of Engineering in Nigeria (COREN). His multidisciplinary engineering experience reflects a strong command of both field and regulatory practices within the civil and structural engineering sectors",
  },
  {
    name: "Engr. Igata Cosmas Chijioke",
    role: "Engr. Igata is a seasoned Civil Engineer with a B.Eng. and several professional certifications. He is a Member of the Nigeria Institute of Management (MNIM), a Graduate and Corporate Member of the Nigeria Society of Engineers (NSE), and registered with COREN. His commitment to technical excellence is backed by years of experience and strong industry affiliations",
  },
  {
    name: "Engr. Adah Noah Abuh",
    role: "With a Higher National Diploma (HND) in Civil Engineering, Engr. Adah is a Corporate Member of the Nigeria Society of Engineers (MNSE), the Nigeria Association of Technologists in Engineering (MNATE), and COREN. His broad technical knowledge and professional standing reflect a solid foundation in engineering practice and supervision",
  },
  {
    name: "Engr. Elochukwu Kenneth Okafor",
    role: "Engr. Elochukwu is a skilled Civil Engineer and a registered member of both the Council for the Regulation of Engineering in Nigeria (COREN) and the Nigeria Society of Engineers (NSE). His career reflects a deep commitment to quality engineering solutions and infrastructure development",
  },
  {
    name: "Engr. Okorie Chinomso C.",
    role: "Engr. Okorie holds a B.Eng. in Civil Engineering and has completed the NYSC. He is a Proficiency Certificate holder in Management and a member of multiple professional bodies, including the Nigeria Society of Engineers (MNSE), Nigeria Institute of Civil Engineering (NICE), and the Nigeria Institute of Management (GMNIM). His blend of engineering and managerial skills positions him as a valuable asset in both technical and administrative project role",
  }
]

const activeIndex = ref(null);

const toggleExpanded = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index;
};
</script>

<style scoped>
.team-card {
  @apply flex flex-col p-6 rounded-lg transition-transform duration-300 bg-gray-100 dark:bg-red-900;
  backdrop-filter: blur(10px);
}

.icon {
  @apply p-2 rounded-full bg-gray-800 hover:bg-gray-700 dark:bg-gray-600 dark:hover:bg-gray-500 transition-all;
}

.line-clamp-2 {
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

</style>