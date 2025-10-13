<script setup>
import { computed } from 'vue';
import { Sun, MoonStar } from 'lucide-vue-next';
import { useColorMode } from '@vueuse/core';

const mode = useColorMode();

const isDarkMode = computed(() => mode.value === 'dark');

function toggleTheme() {
  mode.value = isDarkMode.value ? 'light' : 'dark';
}
</script>

<template>
  <button 
    @click="toggleTheme" 
    class="cursor-pointer rounded-full p-2 bg-[#ffb029] dark:bg-white dark:text-black text-white backdrop-blur-2xl hover:scale-110 transition-all" 
    aria-label="Cambiar entre modo oscuro y claro"
  >
    <Sun v-if="isDarkMode" />
    <MoonStar v-else />
  </button>
</template>