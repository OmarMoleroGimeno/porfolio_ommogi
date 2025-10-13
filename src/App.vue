<script setup lang="ts">
import { computed } from 'vue';
import { useDark } from '@vueuse/core';

import DotGrid from '@/components/Backgrounds/DotGrid/DotGrid.vue';
import { ArrowBigDownDash } from 'lucide-vue-next';

import Presentacion from './components/Presentation/Presentacion.vue';
import HeaderComponent from './components/Header/HeaderComponent.vue';

const isDark = useDark();
const dotGridBaseColor = computed(() => {
  return isDark.value ? '#333333' : '#bdbdbd';
});

</script>

<template>
  <div class="relative w-full min-h-screen overflow-hidden">
    <div class="absolute inset-0 z-0">
      <DotGrid
        :dot-size="3"
        :gap="15"
        :base-color="dotGridBaseColor" active-color="#ffb029"
        :proximity="150"
        :speed-trigger="100"
        :shock-radius="250"
        :shock-strength="5"
        :max-speed="5000"
        :resistance="750"
        :return-duration="1.5"
        class-name="w-full h-full dark:bg-[#0b0b0b] bg-[#f0f0f0]"
      />
    </div>
    
    <div class="relative z-10">
      <header class="flex align-middle justify-center">
        <HeaderComponent />
      </header>
      <main class="max-w-[1200px] mx-auto flex items-center justify-between">
          <Presentacion />
      </main>
    </div>
    <ArrowBigDownDash class="absolute bottom-5 left-1/2 -translate-x-1/2 w-10 h-10 text-[#ffb029] animate-bounce-y" />
  </div>
</template>
<style>
@keyframes bounce-y {
  0%, 100% {
    transform: translateY(-25%);
    animation-timing-function: cubic-bezier(0.8, 0, 1, 1);
  }
  50% {
    transform: translateY(0);
    animation-timing-function: cubic-bezier(0, 0, 0.2, 1);
  }
}

.animate-bounce-y {
  animation: bounce-y 2s infinite;
}
</style>