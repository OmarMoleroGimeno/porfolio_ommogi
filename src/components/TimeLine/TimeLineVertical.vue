<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true
  },
  timelineEvents: {
    type: Array,
    required: true
  }
});
</script>

<template>
  <section class="max-w-3xl p-8 mx-auto">
    <h2 class="flex justify-center text-4xl font-bold">{{ title }}</h2>
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
          <h3 class="text-lg ">{{ event.instituto }}</h3>
          <p class="text-sm font-semibold text-[#3d3d3d] mb-2">{{ event.year }}</p>
          <p class="text-[#6b6b6b]">{{ event.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>