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
  <section class="max-w-[1400px] p-8 mx-auto mt-16">
    <h2 class="flex justify-center text-4xl font-bold mb-16">{{ title }}</h2>
    
    <div class="relative pb-12 pt-12 my-[150px]">
      
      <div class="absolute top-1/2 left-0 right-0 h-[1px] bg-[#6b6b6b] -translate-y-1/2 z-0"></div>
      
      <div class="flex justify-between items-center w-full relative gap-48">
        
        <div 
          v-for="event in timelineEvents"
          :key="event.id"
          class="relative flex flex-col items-center flex-1"
        >
          <div class="w-6 h-6 bg-[#ffb029] border-[6px] dark:border-[#0b0b0b] border-[#f0f0f0] rounded-full z-10"></div>
          
          <div :class="[
                'p-6 rounded-lg w-80 absolute',
                event.id % 2 === 0 ? 'bottom-8' : 'top-8'
              ]">
            <h3 class="text-2xl text-[#fdbf53] text-center">{{ event.title }}</h3>
            <h3 class="text-lg text-center">{{ event.instituto }}</h3>
            <p class="text-sm font-semibold text-[#6b6b6b] mb-2 text-center">{{ event.year }}</p>
            <p class="text-center">{{ event.text }}</p>
          </div>
        </div>
        
      </div>
    </div>
  </section>
</template>