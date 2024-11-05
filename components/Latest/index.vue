<template>
  <section
    class="bg-white shadow-md p-6 max-w-6xl mx-auto px-6 sm:px-2 w-full -mt-12 sm:-mt-16 lg:-mt-20 relative z-10"
  >
    <div class="max-w-6xl mx-7 px-4 py-6 bg-white">
      <!-- Section Header -->
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-xl font-bold text-yellow-700">Latest Music</h2>
        <button class="text-yellow-700 pr-4 mr-4">Voir Tout</button>
      </div>

      <!-- Music Card List -->
      <div class="space-y-6">
        <!-- Music Card Item -->
        <div
          v-for="(music, index) in musicList"
          :key="index"
          class="flex items-start p-4 border-b-2 hover:shadow-lg transition duration-300"
        >
          <!-- Thumbnail -->
          <img
            :src="music.thumbnail"
            alt="Cover Image"
            class="w-20 h-20 rounded-lg mr-4 object-cover"
          />

          <!-- Music Details -->
          <div class="flex-1">
            <h3
              class="text-gray-800 font-semibold text-sm lg:text-base uppercase"
            >
              {{ music.artist }}
            </h3>
            <p class="text-gray-600 text-sm">{{ music.title }}</p>
            <p class="text-xs text-gray-500 mt-1">{{ music.description }}</p>

            <!-- Stats -->
            <div class="flex items-center space-x-3 text-xs text-gray-400 mt-2">
              <span
                ><i class="fas fa-headphones"></i>
                {{ music.stats.listenCount }}</span
              >
              <span
                ><i class="fas fa-thumbs-up"></i>
                {{ music.stats.likeCount }}</span
              >
              <span
                ><i class="fas fa-share"></i> {{ music.stats.shareCount }}</span
              >
              <span
                ><i class="fas fa-download"></i>
                {{ music.stats.downloadCount }}</span
              >
            </div>
          </div>

          <!-- Play Button -->
          <button
            class="flex items-center justify-center w-8 h-8 rounded-full border border-gray-300 text-gray-700 hover:bg-yellow-700 hover:text-white transition duration-300 ml-4"
          >
            <i class="fas fa-play"></i>
          </button>
        </div>
      </div>

      <!-- View More Button -->
      <div class="mt-6 text-center">
        <button
          class="bg-black text-yellow-300 px-6 py-2 hover:bg-gray-800 transition duration-300"
        >
          Voir plus des singles
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      musicList: [
        {
          artist: "SHEKINAH MPIANA",
          title: "Désormais",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          thumbnail: "/images/desormais.jpg",
          stats: {
            listenCount: "8.9K",
            likeCount: "2.1K",
            shareCount: "982K",
            downloadCount: "284K",
          },
        },
        {
          artist: "LORD LOMBO",
          title: "CELEBRONS HEBRON AUJOURD'HUI",
          description: "Quisque sit amet lacus luctus, ultrices eros ac.",
          thumbnail: "/images/celebrons.jpg",
          stats: {
            listenCount: "24K",
            likeCount: "3.2K",
            shareCount: "5.6K",
            downloadCount: "1.9K",
          },
        },
        {
          artist: "FAVEUR MUKOKO",
          title: "Hakuniasha",
          description: "Cras facilisis orci in arcu ullamcorper viverra.",
          thumbnail: "/images/hakuniasha.jpg",
          stats: {
            listenCount: "42K",
            likeCount: "10K",
            shareCount: "16K",
            downloadCount: "5.1K",
          },
        },
      ],
    };
  },
};
</script>

<style scoped>
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
