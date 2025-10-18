<script setup>
import spotifyStats from '@/assets/img/proyectos/spotifyStats.png';
import Vue from "@/assets/img/skills/vue.svg";
import Pinia from "@/assets/img/skills/pinia.svg";
import GoLinkButton from '@/components/Buttons/GoLinkButton.vue';
import TailwindCSS from '@/assets/img/skills/tailwindcss.svg';
import { ArrowUpRight } from 'lucide-vue-next';


</script>
<template>
    <div @click="" class="group border hover:cursor-pointer border-[#333333] rounded-2xl backdrop-blur-lg max-w-[25rem] bg-[#0b0b0b] hover:border-[#585858] transition-colors relative">
        <div class="absolute top-4 right-4 opacity-0 group-hover:opacity-100 transition-opacity z-10">
            <ArrowUpRight />
        </div>
        <div class="relative">
            <img :src="spotifyStats" class="rounded-t-2xl w-[25rem]" alt="">
            <div class="absolute bottom-0 left-0 right-0 h-16 bg-gradient-to-t from-[#0b0b0b] to-transparent"></div>
        </div>
        <div class="p-4">
            <h4 class="text-xl mb-2">Spotify Stats</h4>
            <p class="mb-4 text-[#7c7c7c]  ">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo ab dolorem, minus iure, neque, ipsam harum pariatur architecto eos eaque at magni doloribus! Laudantium nihil, minima quisquam ut vero ipsum!</p>
            <div class="flex justify-between  items-center">
                <div class="flex flex-row gap-4">
                    <img :src="Vue" class="h-6" alt="">
                    <img :src="Pinia" class="h-6" alt="">
                    <img :src="TailwindCSS" class="h-6" alt="">
                </div> 
                <div class="mt-2">
                    <GoLinkButton text="github" url="https://github.com/OmarMoleroGimeno/stats-spotify">
                        <svg viewBox="0 0 192 192" xmlns="http://www.w3.org/2000/svg" height="25" fill="none">
                        <path class="dark:stroke-black stroke-white"stroke-linecap="round" stroke-linejoin="round" stroke-width="12" 
                            d="M120.755 170c.03-4.669.059-20.874.059-27.29 0-9.272-3.167-15.339-6.719-18.41 
                            22.051-2.464 45.201-10.863 45.201-49.067 0-10.855-3.824-19.735-10.175-26.683 
                            1.017-2.516 4.413-12.63-.987-26.32 0 0-8.296-2.672-27.202 10.204-7.912-2.213-16.371-3.308-24.784-3.352
                            -8.414.044-16.872 1.14-24.785 3.352C52.457 19.558 44.162 22.23 44.162 22.23
                            c-5.4 13.69-2.004 23.804-.987 26.32C36.824 55.498 33 64.378 33 75.233
                            c0 38.204 23.149 46.603 45.2 49.067-3.551 3.071-6.719 9.138-6.719 18.41
                            0 6.416.03 22.621.059 27.29M27 130c9.939.703 15.67 9.735 15.67 9.735
                            8.834 15.199 23.178 10.803 28.815 8.265">
                        </path>
                        </svg>
                        <!-- <span>Ver Repositorio</span> -->
                    </GoLinkButton>
                </div>
            </div>
        </div>
    </div>
</template>