<script setup>
import TimeLineHoritzaontal from '@/components/TimeLine/TimeLineHoritzaontal.vue';

const timelineEvents = [
  { id: 1, year: '2021 - 2023', title: 'Bachillerato', instituto:"I.E.S Mestre Ramón Esteve" },
  { id: 2, year: '2023 - 2025', title: 'FPGS Desarollo de Aplicaciones WEB', instituto:"I.E.S Mestre Ramón Esteve" },
  { id: 3, year: '2025 - Presente', title: 'Ingeniería informática', instituto:"UPV Universitat Politècnica de València" },
];
</script>

<template>
  <TimeLineHoritzaontal :timeline-events="timelineEvents" title="Estúdios" />
</template>