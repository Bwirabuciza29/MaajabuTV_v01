<template>
  <section class="bg-white px-10 py-6 max-w-6xl mx-auto w-full">
    <div class="bg-white max-w-6xl mx-4 sm:mx-2 py-6 px-4">
      <!-- Section Header -->
      <div class="flex items-center justify-between border-gray-200 py-4">
        <div
          class="w-1/3 sm:w-[35%] border-t border-gray-300 ml-4 mr-1 hidden sm:block"
        ></div>
        <h2
          class="text-xl sm:text-3xl font-bold text-yellow-500 transform transition duration-200 hover:scale-105"
        >
          Albums
        </h2>
        <div
          class="w-1/3 sm:w-[35%] border-t border-gray-300 ml-4 mr-1 hidden sm:block"
        ></div>
      </div>
      <!-- Fin Section Header -->
    </div>
    <!-- Fin titre -->
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
  max-width: 640px;
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
