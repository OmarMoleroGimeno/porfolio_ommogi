<script setup>
import PillNav from '@/components/Components/PillNav/PillNav.vue';
import DarkMode from '@/components/DarkMode/DarkMode.vue';

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
        pillColor="#ffffff"
        hoveredPillTextColor="#ffffff"
        pillTextColor="#000000"
    />
    <DarkMode class="absolute top-[1em] right-8" />
</template>