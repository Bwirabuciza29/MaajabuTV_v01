<template>
  <section
    class="bg-white shadow-md px-10 py-6 max-w-6xl mx-auto w-full relative z-10 -mt-12 sm:-mt-16 lg:-mt-20"
  >
    <div class="bg-white max-w-6xl mx-4 sm:mx-2 py-6 px-4">
      <!-- Section Header -->
      <div
        class="flex items-center justify-between border-b border-gray-200 py-4"
      >
        <h2 class="text-xl sm:text-2xl font-bold text-yellow-500">
          Latest Music
        </h2>
        <button
          class="border border-yellow-400 text-yellow-500 px-3 sm:px-4 py-1 sm:py-2 text-xs sm:text-sm font-medium hover:bg-yellow-50 transition duration-200"
        >
          Voir Tout
        </button>
      </div>
      <!-- Fin Section Header -->

      <!-- Liste des cards -->
      <div class="py-6 space-y-8">
        <div
          v-for="episode in episodes"
          :key="episode.id"
          class="flex flex-col md:flex-row items-start space-y-4 md:space-y-0 md:space-x-4 border-b pb-4"
        >
          <!-- Image de l'album -->
          <img
            :src="episode.image"
            alt="Album cover"
            class="w-24 h-24 sm:w-32 sm:h-32 md:w-40 md:h-40 object-cover transition-transform duration-300 hover:scale-105"
          />

          <!-- Informations de l'épisode -->
          <div class="flex-1">
            <!-- Conteneur avec hover global sur tout le texte -->
            <div
              class="text-xs sm:text-sm text-gray-500 flex flex-wrap items-center space-x-1 hover:text-yellow-500 hover:underline hover:translate-y-[-3px] transition-all duration-300"
            >
              <span>{{ episode.artist }}</span>
              <span class="mx-1 hidden sm:inline">•</span>
              <span>{{ episode.duration }}</span>
              <span class="mx-1 hidden sm:inline">•</span>
              <span>Episode {{ episode.episode }}</span>
            </div>

            <!-- Titre -->
            <h3
              class="text-base sm:text-lg font-semibold mt-1 hover:text-yellow-500 hover:underline hover:translate-y-[-3px] transition-all duration-300"
            >
              {{ episode.title }}
            </h3>

            <!-- Description -->
            <p
              class="text-gray-600 mt-1 text-xs sm:text-sm hover:text-yellow-500 hover:underline hover:translate-y-[-3px] transition-all duration-300"
            >
              {{ episode.description }}
            </p>

            <!-- Statistiques de l'épisode -->
            <div
              class="flex flex-wrap items-center space-x-3 text-gray-400 mt-3"
            >
              <div class="flex items-center space-x-1 sm:space-x-2">
                <img
                  src="assets/img/icons/Headphones.svg"
                  alt="Headphones"
                  class="w-4 h-4 sm:w-5 sm:h-5"
                />
                <span class="text-xs sm:text-sm">{{
                  episode.stats.listen
                }}</span>
              </div>
              <div class="flex items-center space-x-1 sm:space-x-2">
                <img
                  src="assets/img/icons/fi_heart.svg"
                  alt="heart"
                  class="w-4 h-4 sm:w-5 sm:h-5"
                />
                <span class="text-xs sm:text-sm">{{
                  episode.stats.likes
                }}</span>
              </div>
              <div class="flex items-center space-x-1 sm:space-x-2">
                <img
                  src="assets/img/icons/Chat.svg"
                  alt="comment"
                  class="w-4 h-4 sm:w-5 sm:h-5"
                />
                <span class="text-xs sm:text-sm">{{
                  episode.stats.comments
                }}</span>
              </div>
              <div class="flex items-center space-x-1 sm:space-x-2">
                <img
                  src="assets/img/icons/fi_download.svg"
                  alt="download"
                  class="w-4 h-4 sm:w-5 sm:h-5"
                />
                <span class="text-xs sm:text-sm">{{
                  episode.stats.downloads
                }}</span>
              </div>
            </div>
          </div>

          <!-- Bouton Lecture centré en dessous -->
          <button
            class="flex self-center items-center justify-center w-14 h-14 sm:w-16 sm:h-16 bg-gray-200 rounded-full mt-10 hover:bg-yellow-300 hover:scale-105 transition-colors duration-300 ease-in-out"
          >
            <img
              src="assets/img/frame 4.png"
              alt="Play icon"
              class="w-6 h-6 sm:w-8 sm:h-8"
            />
          </button>
        </div>
      </div>

      <!-- View More Button -->
      <div class="mt-6 text-center">
        <button
          class="bg-black text-yellow-300 px-4 py-2 sm:px-6 sm:py-3 text-sm sm:text-base hover:bg-gray-800 transition duration-300"
        >
          Voir plus des singles
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
