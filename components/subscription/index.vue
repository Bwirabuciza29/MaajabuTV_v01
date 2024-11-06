<!-- pages/subscription.vue -->
<template>
  <div
    class="flex items-center justify-center min-h-screen bg-pattern bg-cover bg-center p-4"
  >
    <div
      class="bg-black bg-opacity-80 text-center text-white p-8 rounded-lg max-w-md w-full"
    >
      <h1 class="text-2xl font-bold mb-4">
        Nouvel épisode<br />chaque semaine
      </h1>
      <p class="text-gray-300 mb-6">
        Les dernières mises à jour directement dans votre boîte de réception.
      </p>
      <form @submit.prevent="handleSubscribe" class="flex flex-col space-y-4">
        <input
          type="email"
          placeholder="Add your email here"
          v-model="email"
          class="px-4 py-2 rounded bg-gray-800 text-white placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-yellow-500"
          required
        />
        <button
          type="submit"
          class="px-4 py-2 rounded bg-yellow-500 text-black font-semibold hover:bg-yellow-600 focus:outline-none focus:ring-2 focus:ring-yellow-500"
        >
          Subscribe
        </button>
      </form>
    </div>
  </div>
</template>

<script setup>
// Define a data property for the email
import { ref } from "vue";
const email = ref("");

// Define a submit handler for the form
const handleSubscribe = () => {
  alert(`Subscribed with ${email.value}`);
};
</script>

<style>
.bg-pattern {
  background-image: url("public/img/subBg.png");
}
</style>
