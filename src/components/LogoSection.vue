<template>
  <v-sheet class="d-flex align-center justify-center py-15 ga-5">
    <img
      v-for="item in banners"
      :key="item"
      :src="item"
    >
  </v-sheet>
</template>

<script setup>
const banners = [
  "./assets/banner/csswinner.png",
  "./assets/banner/cssawards.png",
  "./assets/banner/fwa.png",
  "./assets/banner/cssdesignawards.png",
];
</script>
