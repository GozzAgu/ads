<template>
  <section class="bg-gray-100 dark:bg-black min-h-screen">
    <div class="relative w-full h-72 flex items-center justify-center bg-gray-900 text-white">
      <div class="text-center">
        <h1 class="text-4xl md:text-5xl font-bold">Contact Us</h1>
        <p class="mt-2 text-lg text-gray-300">Reach out to us.</p>
      </div>
    </div>

    <div class="bg-white dark:bg-gray-900 rounded-lg shadow-lg p-6 md:p-8 max-w-2xl mx-auto my-12">
      <h3 class="text-xl font-semibold text-gray-900 dark:text-gray-100 mb-4">Get in Touch</h3>
      <p class="text-sm text-gray-600 dark:text-gray-300 mb-6">
        Feel free to contact us for inquiries, collaborations, or general questions.
      </p>
      <form @submit.prevent="handleSubmit">
        <div class="mb-4">
          <label for="name" class="block text-gray-700 dark:text-gray-300 text-sm font-medium mb-2">Your Name</label>
          <input v-model="form.name" type="text" id="name" required class="w-full px-4 py-2 rounded-md border dark:bg-gray-700" />
        </div>
        <div class="mb-4">
          <label for="email" class="block text-gray-700 dark:text-gray-300 text-sm font-medium mb-2">Your Email</label>
          <input v-model="form.email" type="email" id="email" required class="w-full px-4 py-2 rounded-md border dark:bg-gray-700" />
        </div>
        <div class="mb-4">
          <label for="message" class="block text-gray-700 dark:text-gray-300 text-sm font-medium mb-2">Your Message</label>
          <textarea v-model="form.message" id="message" rows="5" required class="w-full px-4 py-2 rounded-md border dark:bg-gray-700"></textarea>
        </div>
        <div class="text-center">
          <button type="submit" class="bg-blue-600 text-white px-6 py-2 rounded-md font-semibold hover:bg-blue-700">Send Message</button>
        </div>
      </form>
    </div>

    <div class="max-w-6xl mx-auto py-16 px-6">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="bg-white dark:bg-gray-900 p-6 rounded-lg shadow-md">
          <h4 class="text-lg font-semibold text-gray-900 dark:text-gray-100">Our Address</h4>
          <p class="text-sm text-gray-600 dark:text-gray-300 mt-2">No 10, Durban street off Adetokunbo Ademola crescent, Wuse II, Abuja, Nigeria.</p>
          <h4 class="text-lg font-semibold text-gray-900 dark:text-gray-100 mt-4">Email</h4>
          <p class="text-sm text-gray-600 dark:text-gray-300">info@visionistrauss.com</p>
          <h4 class="text-lg font-semibold text-gray-900 dark:text-gray-100 mt-4">Phone</h4>
          <p class="text-sm text-gray-600 dark:text-gray-300">+234 703 300 9900 | +234 808 010 0084</p>
        </div>
        <div class="rounded-lg overflow-hidden shadow-lg">
          <iframe
            class="w-full h-96"
            frameborder="0"
            scrolling="no"
            marginheight="0"
            marginwidth="0"
            loading="lazy"
            allowfullscreen
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3939.5964422307023!2d7.48896201428546!3d9.082427693491135!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x104e0a5a05555555%3A0xdec0f92d1a6df28e!2s10%20Durban%20St%2C%20Wuse%2C%20Abuja!5e0!3m2!1sen!2sng!4v1713280032013!5m2!1sen!2sng">
          </iframe>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const form = ref({ name: '', email: '', message: '' });

const handleSubmit = () => {
  console.log('Form submitted:', form.value);
  alert('Message sent! Thank you for contacting us.');
  form.value = { name: '', email: '', message: '' };
};
</script>