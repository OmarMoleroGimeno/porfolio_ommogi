<script setup>
const props = defineProps({
  url: String,
  text: String
});

function goToURL() {
  window.location.href = props.url;
}
</script>
<template>
  <button 
    :title="props.text"
    class="h-10 w-10 border rounded-full border-lightGrey 
           hover:bg-lightGrey text-black dark:text-white transition-all 
           duration-300 transform hover:scale-110 flex 
           items-center justify-center hover:cursor-pointer backdrop-blur-2xl
           hover:shadow-neon"
    @click='goToURL()'
  >
    <slot></slot>
  </button>
</template>
<style>
.hover\:shadow-neon:hover {
  box-shadow: 
    0 0 10px rgba(147, 197, 253, 0.5),
    0 0 20px rgba(147, 197, 253, 0.4),
    0 0 30px rgba(147, 197, 253, 0.3),
    0 0 40px rgba(147, 197, 253, 0.2);
  border-color: rgba(147, 197, 253, 0.8);
}
</style>