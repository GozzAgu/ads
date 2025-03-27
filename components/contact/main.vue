<template>
  <section class="bg-gray-100 dark:bg-gray-900 min-h-screen">
    <div class="relative w-full h-72 flex items-center justify-center bg-gray-800 text-white">
      <div class="text-center">
        <h1 class="text-4xl md:text-5xl font-bold">Contact Us</h1>
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

    <div class="max-w-6xl mx-auto py-16">
      <h3 class="text-2xl font-bold text-gray-800 text-center mb-6">Find Us Here</h3>
      <div class="rounded-lg overflow-hidden shadow-lg">
        <iframe
          class="w-full h-96"
          frameborder="0"
          scrolling="no"
          marginheight="0"
          marginwidth="0"
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d31839.68591437165!2d7.0103419!3d4.8068424!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1069cd9ad68d8c6d%3A0xf74c3b8a6b6d9e4b!2s88%20Evo%20Rd%2C%20GRA%2C%20Port%20Harcourt%2C%20Rivers!5e0!3m2!1sen!2sng!4v1642024158442!5m2!1sen!2sng">
        </iframe>
      </div>
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