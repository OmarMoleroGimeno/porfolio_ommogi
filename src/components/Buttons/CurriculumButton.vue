<script setup>
import { FileUser } from 'lucide-vue-next';
import { saveAs } from 'file-saver';

function descargarCV() {
    saveAs('/curriculum.pdf', 'curriculum.pdf');
  }
</script>
<template>
    <button @click="descargarCV()" class="py-1 px-2 border text-black dark:text-white rounded-md hover:bg-lightGrey transition-all 
           duration-300 transform hover:scale-110 flex 
           items-center justify-center hover:cursor-pointer backdrop-blur-2xl
           hover:shadow-neon gap-2" title="Descargar CV"> 
      Descargar CV
      <FileUser />
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