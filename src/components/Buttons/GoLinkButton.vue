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
    class=" p-2 rounded-full 
           bg-white text-black  text-sm transition-all 
           duration-300 transform hover:scale-110 flex 
           items-center justify-center hover:cursor-pointer backdrop-blur-2xl
           hover:shadow-neon"
    @click='goToURL()'
  >
    <slot></slot>
  </button>
</template>