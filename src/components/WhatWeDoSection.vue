<template>
  <v-sheet
    color="#F1FAFF"
    class="py-15 text-center"
    height="500px"
  >
    <div class="text-h4 font-weight-bold">
      What We Do
    </div>
    <div class="text-body-1 font-weight-regular mt-3 text-grey-darken-2">
      Discover how our amazing team can help your business.
    </div>
    <v-row class="ma-5">
      <v-col
        v-for="item in whatWeDo"
        :key="item.title"
        class="d-flex flex-column align-center"
      >
        <img :src="item.icon">
        <div class="text-h6 mt-1">
          {{ item.title }}
        </div>
        <div class="text-body-1 mt-2 text-grey-darken-2 w-75">
          {{ item.description }}
        </div>
      </v-col>
    </v-row>
  </v-sheet>
</template>

<script setup>
const whatWeDo = [
  {
    icon: "./assets/what/analytics.png",
    title: "Google Analitycs",
    description:
      "Curabitur quam etsum lacus net netsum nulat iaculis etsimun vitae etsum nisle varius netsum",
  },
  {
    icon: "./assets/what/awareness.png",
    title: "Brand Awareness",
    description:
      "Curabitur quam etsum lacus net netsum nulat iaculis etsimun vitae etsum nisle varius netsum",
  },
  {
    icon: "./assets/what/design.png",
    title: "Graphic Design",
    description:
      "Curabitur quam etsum lacus net netsum nulat iaculis etsimun vitae etsum nisle varius netsum",
  },
];
</script>
