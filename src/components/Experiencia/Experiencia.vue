<script setup>
import TimeLineVertical from '@/components/TimeLine/TimeLineVertical.vue';

const timelineEvents = [
  { id: 1, year: '2024', title: 'Desarrollador frontend (GEINFOR)', instituto:"Gestoria informática - Contrato prácticas (DUAL)", text: "Trabajé en el desarrollo de la interfaz de usuario con contrato de prácticas DUAL de 200h para la plataforma de Geinfor, una empresa de software de gestión. Mi labor principal fue el desarrollo de pruebas automatizadas con cypress, y en menor escala, desarrollo de componentes con Angular para el software." },
  { id: 2, year: '2025', title: 'Desarrollador frontend (GEINFOR)', instituto:"Gestoria informática- Contrato prácticas", text: "Trabajé en el desarrollo de la interfaz de usuario con contrato de prácticas 400h para la plataforma de Geinfor. Mi labor principal fue el desarrollo de la interfaz de usuario del software de gestión de esta empresa y detección y arreglo de errores, por otra parte en menor escala, desarrollo de pruebas automatizadas con cypress." },
];
</script>

<template>
  <TimeLineVertical :timeline-events="timelineEvents" title="Experiencia" />
</template>