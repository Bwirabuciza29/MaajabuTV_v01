<template>
  <header
    class="rm-container w-full p-6 flex justify-between items-center z-50"
  >
    <img src="~/assets/img/logo.png" alt="Maajabu Logo" class="h-24" />

    <!-- Menu Desktop -->
    <div class="flex-grow">
      <nav class="hidden md:flex justify-center font-semibold space-x-6">
        <a
          v-for="(item, index) in menuItems"
          :key="index"
          href="#"
          class="hover:text-yellow-400 transition duration-300 hover:underline"
          :class="{ 'text-yellow-500': index === 0 }"
        >
          {{ item }}
        </a>
      </nav>
    </div>

    <!-- LangSwitcher à droite (visible sur desktop) -->
    <LangSwitcher class="hidden md:block" />

    <!-- Bouton Toggle Menu Mobile toujours visible -->
    <button
      @click="toggleMenu"
      class="md:hidden text-yellow-500 fixed top-6 right-6 z-50"
    >
      <svg
        v-if="!menuOpen"
        xmlns="http://www.w3.org/2000/svg"
        class="h-8 w-8"
        viewBox="0 0 20 20"
        fill="currentColor"
      >
        <path
          fill-rule="evenodd"
          d="M3 5h14a1 1 0 010 2H3a1 1 0 110-2zm0 4h14a1 1 0 110 2H3a1 1 0 110-2zm0 4h14a1 1 0 110 2H3a1 1 0 110-2z"
          clip-rule="evenodd"
        />
      </svg>
      <svg
        v-else
        xmlns="http://www.w3.org/2000/svg"
        class="h-8 w-8"
        viewBox="0 0 20 20"
        fill="currentColor"
      >
        <path
          fill-rule="evenodd"
          d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
          clip-rule="evenodd"
        />
      </svg>
    </button>

    <!-- Menu Mobile -->
    <transition name="fade">
      <nav
        v-if="menuOpen"
        class="fixed inset-0 bg-gradient-to-b from-black via-black/70 to-black/40 backdrop-blur-lg border border-gray-700 rounded-lg m-4 p-8 flex flex-col items-center space-y-6 flex-grow transition-transform duration-300 ease-out z-40"
      >
        <a
          v-for="(item, index) in menuItems"
          :key="index"
          href="#"
          class="font-semibold hover:text-yellow-400 text-2xl transition-opacity duration-300 opacity-0 animate-fadeIn delay-{{ index * 100 }} hover:underline"
        >
          {{ item }}
        </a>
        <!-- LangSwitcher à l'intérieur du menu mobile -->
        <LangSwitcher class="block md:hidden mt-4" />
      </nav>
    </transition>
  </header>
</template>

<script setup>
const { t } = useI18n();
const menuOpen = ref(false);

// Méthode pour basculer l'état du menu
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};

// Définir les éléments de menu en utilisant la fonction de traduction
const menuItems = ref([
  t("menu.home"),
  t("menu.news"),
  t("menu.events"),
  t("menu.apps"),
  t("menu.prod"),
  t("menu.about"),
]);
</script>
