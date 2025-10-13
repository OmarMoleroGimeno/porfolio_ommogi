<script setup>
import PillNav from '@/components/Components/PillNav/PillNav.vue';
import DarkMode from '@/components/DarkMode/DarkMode.vue';
import { useDark } from '@vueuse/core';
import { computed } from 'vue';

const isDark = useDark();
const pillColor = computed(() => {
  return isDark.value ? '#0b0b0b' : '#ffffff';
});

import stickerUrl from '@/assets/sticker-omar.png';
</script>
<template>
    <PillNav
        :logo="stickerUrl"
        logoAlt="Company Logo"
        :items="[
        { label: 'Home', href: '/' },
        { label: 'About', href: '/about' },
        { label: 'Services', href: '/services' },
        { label: 'Contact', href: '/contact' }
        ]"
        activeHref="/"
        class="custom-nav"
        ease="power2.easeOut"
        baseColor="#ffb029"
        :pillColor="pillColor"
        hoveredPillTextColor="#ffffff"
        pillTextColor="ffffff"
    />
    <DarkMode class="absolute top-[1em] right-8" />
</template>