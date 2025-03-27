<template>
  <section class="bg-gray-100 dark:bg-gray-900 min-h-screen">
    <div class="relative w-full h-72 flex items-center justify-center bg-gray-800 text-white">
      <div class="text-center">
        <h1 class="text-4xl md:text-5xl font-bold">Our Services</h1>
        <p class="mt-2 text-lg text-gray-300">
          Reach out to us.
        </p>
      </div>
    </div>

    <div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6 md:p-8 max-w-2xl mx-auto my-12">
      <form @submit.prevent="handleSubmit">
        <div class="mb-4">
          <label for="name" class="block text-gray-700 dark:text-gray-300 text-sm font-medium mb-2">
            Your Name
          </label>
          <input
            v-model="form.name"
            type="text"
            id="name"
            required
            class="w-full px-4 py-2 text-gray-900 dark:text-gray-100 dark:bg-gray-700 rounded-md border border-gray-300 dark:border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <div class="mb-4">
          <label for="email" class="block text-gray-700 dark:text-gray-300 text-sm font-medium mb-2">
            Your Email
          </label>
          <input
            v-model="form.email"
            type="email"
            id="email"
            required
            class="w-full px-4 py-2 text-gray-900 dark:text-gray-100 dark:bg-gray-700 rounded-md border border-gray-300 dark:border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <div class="mb-4">
          <label for="message" class="block text-gray-700 dark:text-gray-300 text-sm font-medium mb-2">
            Your Message
          </label>
          <textarea
            v-model="form.message"
            id="message"
            rows="5"
            required
            class="w-full px-4 py-2 text-gray-900 dark:text-gray-100 dark:bg-gray-700 rounded-md border border-gray-300 dark:border-gray-600 focus:outline-none focus:ring-2 focus:ring-blue-500"
          ></textarea>
        </div>

        <div class="text-center">
          <button
            type="submit"
            class="bg-blue-600 text-white px-6 py-2 rounded-md font-semibold hover:bg-blue-700 transition-all"
          >
            Send Message
          </button>
        </div>
      </form>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const form = ref({
  name: '',
  email: '',
  message: ''
});

const handleSubmit = () => {
  console.log('Form submitted:', form.value);
  alert('Message sent! Thank you for contacting us.');
  form.value.name = '';
  form.value.email = '';
  form.value.message = '';
};
</script>