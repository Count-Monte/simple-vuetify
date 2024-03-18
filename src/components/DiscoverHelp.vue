<template>
  <v-sheet
    class="d-flex flex-row align-center justify-space-around"
    height="500px"
  >
    <div>
      <img src="../assets/discover_bg.png">
    </div>
    <div class="w-50">
      <div class="text-h4">
        Discover how we can help you to group your business fast
      </div>
      <div class="text-body-1 text-grey-darken-1 my-5">
        Venis demo enim ipsam voluptatem quia voluptas sit aspernatur netsum
        lorem fugit, seditum netis velas matrix net nesciunt
      </div>
      <div
        v-for="text in discover_text"
        :key="text"
        class="text-grey-darken-1 my-2"
      >
        <v-icon
          icon="mdi-check-bold"
          color="red"
          end
        />
        {{ text }}
      </div>
      <v-btn
        class="ml-5"
        height="55px"
        rounded
        color="#E52F37"
        flat
      >
        Discover More
      </v-btn>
    </div>
  </v-sheet>
</template>

<script setup>
const discover_text = [
  "Quias netus magni netsum eos qui ratione sequi",
  "Venis ratione sequi netus enim quia tempor magne",
  "Venis ratione sequi netus enim quia tempor magne",
];
</script>
