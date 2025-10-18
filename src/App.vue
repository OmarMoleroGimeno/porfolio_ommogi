<script setup lang="ts">
import { computed } from 'vue';
import { useDark } from '@vueuse/core';

import DotGrid from '@/components/Backgrounds/DotGrid/DotGrid.vue';

import Presentacion from '@/components/Presentation/Presentacion.vue';
import HeaderComponent from '@/components/Header/HeaderComponent.vue';
import Skills from '@/components/Skills/Skills.vue';
import Experiencia from '@/components/Experiencia/Experiencia.vue';
import Estudios from '@/components/Estudios/Estudios.vue';
import Proyectos from '@/components/Proyectos/Proyectos.vue';

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
        :gap="20"
        :base-color="dotGridBaseColor" active-color="#ffb029"
        :proximity="100"
        :speed-trigger="100"
        :shock-radius="150"
        :shock-strength="5"
        :max-speed="5000"
        :resistance="2000"
        :return-duration="1"
        class-name="w-full h-full dark:bg-[#0b0b0b] bg-[#f0f0f0]"
      />
    </div>
    
    <div class="relative z-10">
      <header class="flex align-middle justify-center">
        <HeaderComponent />
      </header>
      <main class="max-w-[1200px] mx-auto flex flex-col items-start justify-between px-8">
          <Presentacion />
          <Skills />
          <Experiencia />
          <Proyectos />
          <Estudios />
      </main>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Onest:wght@100..900&display=swap');

body {
  font-family: 'Onest', sans-serif;
}
</style>