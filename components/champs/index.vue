<template>
  <section class="bg-white px-10 py-6 max-w-6xl mx-auto w-full">
    <div class="bg-white max-w-6xl mx-4 sm:mx-2 py-6 px-4">
      <!-- Section Header -->
      <div
        class="flex items-center justify-between border-b border-gray-200 py-4"
      >
        <div
          class="w-1/3 sm:w-[35%] border-t border-gray-300 ml-4 mr-1 hidden sm:block"
        ></div>
        <h2
          class="text-xl sm:text-3xl font-bold text-yellow-500 transform transition duration-200 hover:scale-105"
        >
          Plus qu'un champs
        </h2>
        <div
          class="w-1/3 sm:w-[35%] border-t border-gray-300 ml-4 mr-1 hidden sm:block"
        ></div>
      </div>
      <!-- Fin Section Header -->
    </div>
    <!-- Fin titre -->
    <div class="flex flex-cols-3 justify-between md:space-x-2 p-4 md:space-y-0">
      <!-- Musics cards -->
      <div class="relative h-96 overflow-hidden">
        <img
          src="assets/img/c1.jpeg"
          alt="Music"
          class="object-cover w-full h-full transition-all duration-300 hover:scale-110 hover:z-10 hover:shadow-lg"
        />
        <div
          class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-end p-4 text-white backdrop-blur-md"
          style="top: 80%"
        >
          <h2 class="text-xl font-semibold">Music</h2>
          <p class="text-sm">70 CHANNELS</p>
        </div>
      </div>

      <!-- Deuxième ligne avec 3 cartes -->
      <div class="flex flex-wrap w-full md:w-1/3 space-y-2 md:space-y-0">
        <div class="relative w-full h-48 overflow-hidden">
          <img
            src="assets/img/c2.jpg"
            alt="Clip du jours"
            class="object-cover w-full h-full transition-all duration-300 hover:scale-110 hover:z-10 hover:shadow-lg"
          />
          <div
            class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-end p-4 text-white backdrop-blur-md"
            style="top: 65%"
          >
            <h2 class="text-lg font-semibold">Clip du jours</h2>
            <p class="text-sm">55 CHANNELS</p>
          </div>
        </div>

        <div class="flex space-x-2 w-full">
          <!-- Story Life -->
          <div class="relative w-1/2 h-48 overflow-hidden">
            <img
              src="assets/img/c3.jpeg"
              alt="Story Life"
              class="object-cover w-full h-full transition-all duration-300 hover:scale-110 hover:z-10 hover:shadow-lg"
            />
            <div
              class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-end p-4 text-white backdrop-blur-md"
              style="top: 65%"
            >
              <h2 class="text-lg font-semibold">Story Life</h2>
              <p class="text-sm">24 CHANNELS</p>
            </div>
          </div>
          <!-- Concerts -->
          <div class="relative w-1/2 h-48 overflow-hidden">
            <img
              src="assets/img/c4.jpg"
              alt="Concerts"
              class="object-cover w-full h-full transition-all duration-300 hover:scale-110 hover:z-10 hover:shadow-lg"
            />
            <div
              class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-end p-4 text-white backdrop-blur-md"
              style="top: 65%"
            >
              <h2 class="text-lg font-semibold">Concerts</h2>
              <p class="text-sm">14 CHANNELS</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Troisième ligne avec une carte et un bouton -->
      <div class="flex flex-col w-full md:w-1/3 space-y-4">
        <div class="relative h-96 overflow-hidden">
          <img
            src="assets/img/c5.jpeg"
            alt="Music"
            class="object-cover w-full h-full transition-all duration-300 hover:scale-110 hover:z-10 hover:shadow-lg"
          />
          <div
            class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-end p-4 text-white backdrop-blur-md hover:bg-yellow-500 hover:text-black"
            style="top: 80%"
          >
            <h2 class="text-xl font-semibold">Music</h2>
            <p class="text-sm">70 CHANNELS</p>
          </div>
        </div>
        <button class="bg-black text-yellow-500 font-semibold px-4 py-3">
          <span
            class="hover:text-yellow-200 transition duration-300 hover:scale-110"
          >
            Afficher plus de catégorie</span
          >
        </button>
      </div>
    </div>
  </section>
</template>
<script setup>
import pub1 from "../assets/img/a1.png";
import pub2 from "../assets/img/a2.png";
import pub3 from "../assets/img/a3.png";

const episodes = ref([
  {
    id: 1,
    artist: "SHEKINAH MPIANA",
    duration: "46 min",
    episode: 10,
    title: "Désormais",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean ac neque sagittis...",
    image: pub1,
    stats: {
      listen: "8.9K",
      likes: "2.1K",
      comments: "982K",
      downloads: "284K",
    },
  },
  {
    id: 2,
    artist: "LORD LOMBO",
    duration: "34 min",
    episode: 9,
    title: "CELEBRONS HEBRON AUJOURD'HUI",
    description:
      "Quisque sit amet lacus luctus, ultrices eros ac, laoreet sem...",
    image: pub2,
    stats: {
      listen: "24K",
      likes: "3.2K",
      comments: "5.6K",
      downloads: "1.9K",
    },
  },
  {
    id: 3,
    artist: "FAVEUR MUKOKO",
    duration: "46 min",
    episode: 8,
    title: "Hakuniacaha",
    description:
      "Cras facilisis orci in arcu ullamcorper viverra. Maecenas vulputate risus...",
    image: pub3,
    stats: {
      listen: "42K",
      likes: "10K",
      comments: "16K",
      downloads: "5.1K",
    },
  },
]);
</script>


<style scoped>
.container {
  max-width: 640px; /* Limite la largeur pour la responsivité */
}
@media (min-width: 768px) {
  .container {
    max-width: 768px;
  }
}
@media (min-width: 1024px) {
  .container {
    max-width: 1024px;
  }
}

/* Responsive Styles */
@media (max-width: 768px) {
  h2 {
    font-size: 1.25rem;
  }
  .music-card {
    flex-direction: column;
    text-align: center;
  }
  .music-card img {
    width: 100%;
    height: auto;
    margin-bottom: 1rem;
  }
  .music-card .stats {
    justify-content: center;
  }
}
</style>
