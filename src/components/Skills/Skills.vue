<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue';

import vue from '../../assets/img/skills/vue.svg';
import tailwind from '../../assets/img/skills/tailwindcss.svg';
import javascript from '../../assets/img/skills/javascript.svg';
import html from '../../assets/img/skills/html5.svg';
import css from '../../assets/img/skills/css_old.svg';
import git from '../../assets/img/skills/git.svg';
import figma from '../../assets/img/skills/figma.svg';
import angular from '../../assets/img/skills/angular.svg';
import atlassian from '../../assets/img/skills/atlassian.svg';
import cypress from '../../assets/img/skills/cypress.svg';
import docker from '../../assets/img/skills/docker.svg';
import java from '../../assets/img/skills/java.svg';
import laravel from '../../assets/img/skills/laravel.svg';
import pinia from '../../assets/img/skills/pinia.svg';

import github_light from '../../assets/img/skills/github_light.svg';
import github_dark from '../../assets/img/skills/github_dark.svg';
import markdown_light from '../../assets/img/skills/Markdown_light.svg';
import markdown_dark from '../../assets/img/skills/Markdown_dark.svg';

const isDark = ref(false);

const githubIcon = computed(() => {
    return isDark.value ? github_dark : github_light;
});

const markdownIcon = computed(() => {
    return isDark.value ? markdown_dark : markdown_light;
});

onMounted(() => {
    const updateDarkMode = () => {
        isDark.value = document.documentElement.classList.contains('dark');
    };

    updateDarkMode();

    const observer = new MutationObserver(updateDarkMode);
    observer.observe(document.documentElement, {
        attributes: true,
        attributeFilter: ['class'],
    });

    onUnmounted(() => {
        observer.disconnect();
    });
});


const technologies = ref([
    { name: 'Vue', url: vue },
    { name: 'Pinia', url: pinia },
    { name: 'Angular', url: angular },
    { name: 'Laravel', url: laravel },
    { name: 'JavaScript', url: javascript },
    { name: 'Java', url: java },
    { name: 'HTML', url: html },
    { name: 'CSS', url: css },
    { name: 'Tailwind', url: tailwind },
]);

const tools = ref([
    { name: 'Git', url: git },
    { name: 'GitHub', url: githubIcon },
    { name: 'Figma', url: figma },
    { name: 'Docker', url: docker },
    { name: 'Cypress', url: cypress },
    { name: 'Atlassian', url: atlassian },
    { name: 'Markdown', url: markdownIcon },
]);
</script>

<template>
    <section class="w-full py-16">
        <h2 class="text-4xl font-bold mb-12 text-center text-black dark:text-white">Habilidades</h2>

        <div>
            <h3 class="text-2xl font-semibold mb-8 text-black dark:text-white">Tecnologías</h3>
            <div class="grid grid-cols-2 sm:grid-cols-4 md:grid-cols-6 lg:grid-cols-8 gap-8">
                <div v-for="tech in technologies" :key="tech.name" class="flex flex-col items-center justify-center gap-2">
                    <div class="w-20 h-20 p-3 rounded-lg border  border-black/30 dark:border-white/30 bg-gray-200 dark:bg-[#161616] backdrop-blur-md flex items-center justify-center transition-transform hover:scale-110">
                        <img :src="tech.url" :alt="tech.name" class="w-full h-full object-contain" />
                    </div>
                    <span class="text-sm capitalize text-black dark:text-white">{{ tech.name }}</span>
                </div>
            </div>
        </div>

        <div class="mt-16">
            <h3 class="text-2xl font-semibold mb-8 text-black dark:text-white">Herramientas</h3>
            <div class="grid grid-cols-2 sm:grid-cols-4 md:grid-cols-6 lg:grid-cols-8 gap-8">
                <div v-for="tool in tools" :key="tool.name" class="flex flex-col items-center justify-center gap-2">
                    <div class="w-20 h-20 p-3 rounded-lg border border-black/30 dark:border-white/30 bg-gray-200 dark:bg-[#161616] backdrop-blur-md flex items-center justify-center transition-transform hover:scale-110">
                        <img :src="tool.url" :alt="tool.name" class="w-full h-full object-contain" />
                    </div>
                    <span class="text-sm capitalize text-black dark:text-white">{{ tool.name }}</span>
                </div>
            </div>
        </div>
    </section>
</template>