
<template>
  <div
    class="flex items-center justify-center bg-pattern bg-cover bg-center p-4"
  >
    <div class="text-center text-yellow-300 p-8 rounded-lg max-w-md w-full">
      <h1 class="text-3xl font-bold mb-4">
        Nouvel épisode<br />chaque semaine
      </h1>
      <p class="text-gray-300 mb-6">
        Les dernières mises à jour directement dans votre boîte de réception.
      </p>
      <div class="relative max-w-lg mx-auto">
        <input
          type="text"
          class="w-full bg-black py-4 pl-3 pr-16 border border-gray-300 focus:outline-none focus:ring-2"
          placeholder="Entrez du texte"
        />
        <button
          type="submit"
          class="absolute inset-y-0 right-0 px-4 py-2 m-2 bg-yellow-500 text-white hover: focus:outline-none"
        >
          Subscribe
        </button>
      </div>
    </div>
    <hr class="border border-gray-200" />
  </div>
</template>

<script setup>
</script>

<style>
.bg-pattern {
  background-image: url("/img/subBg.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
