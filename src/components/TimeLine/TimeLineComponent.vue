<script setup>
const timelineEvents = [
  { id: 1, year: '2021 - 2023', title: 'Bachillerato', instituto:"I.E.S Mestre Ramón Esteve" },
  { id: 2, year: '2023 - 2025', title: 'FPGS Desarollo de Aplicaciones WEB', instituto:"I.E.S Mestre Ramón Esteve" },
  { id: 3, year: '2025 - Presente', title: 'Ingeniería informática', instituto:"UPV Universitat Politècnica de València" },
];
</script>

<template>
  <section class="max-w-3xl p-8 mx-auto">
    <h2 class="text-4xl">Estúdios</h2>
    <div class="relative flex flex-col gap-y-12 mt-8">
      
      <div class="absolute top-0 w-[1px] h-full -translate-x-1/2 bg-[#6b6b6b]"></div>

      <div 
        v-for="event in timelineEvents"
        :key="event.id"
        class="relative"
      >
        <div class="absolute top-1 w-6 h-6 -translate-x-1/2 bg-[#ffb029] border-[6px] dark:border-[#0b0b0b] border-[#f0f0f0] rounded-full"></div>
        <div class="p-4 pt-2 ml-4 rounded-lg">
          <h3 class="text-2xl text-[#fdbf53]">{{ event.title }}</h3>
          <h3 class="text-lg">{{ event.instituto }}</h3>
          <p class="text-sm font-semibold text-[#6b6b6b] mb-2">{{ event.year }}</p>
        </div>
      </div>
    </div>
  </section>
</template>