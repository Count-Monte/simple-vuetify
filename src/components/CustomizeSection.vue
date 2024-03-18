<template>
  <v-sheet
    class="d-flex flex-row align-center justify-space-around"
    height="500px"
    color="#F1FAFF"
  >
    <v-list
      base-color="transparent"
      bg-color="transparent"
      lines="three"
      variant="flat"
      class="w-50 py-10"
    >
      <v-list-item
        v-for="(item, index) in customize"
        :key="item.title"
        class="ga-5 mx-10"
        :class="{ 'bg-grey-lighten-5 elevation-5 rounded': index === 0 }"
      >
        <template #prepend>
          <img :src="item.icon">
        </template>

        <template #title>
          <span class="text-h6 font-weight-bold">{{ item.title }}</span>
        </template>

        <template #subtitle>
          <span class="text-body-1 text-grey-darken-3">{{
            item.subtitle
          }}</span>
        </template>
      </v-list-item>
    </v-list>
    <div>
      <img
        src="../assets/customize_bg.png"
        class="elevation-5"
      >
    </div>
  </v-sheet>
</template>

<script setup>
const customize = [
  {
    icon: "./assets/customize.png",
    title: "Customize your workflow",
    subtitle:
      "Manage any process and be ready to address any challenge with total ease.",
  },
  {
    icon: "./assets/onboarding.png",
    title: "Easy onboarding, fast adoption.",
    subtitle:
      "With Square getting your team on board is as simple as sending an email.",
  },
  {
    icon: "./assets/retention.png",
    title: "Improve subscriber retention",
    subtitle:
      "Analyze customers by region, discounts and more and put a plan in place.",
  },
];</script>
