<template>
  <v-sheet
    class="text-center pt-15"
    height="800px"
    color="#F1FAFF"
  >
    <div class="text-h4 font-weight-bold">
      Meet Our Team
    </div>
    <div class="text-body-1 text-grey-darken-1 mt-5">
      Discover more about our high performing team.
    </div>
    <v-row class="pa-10">
      <v-col
        v-for="person in team"
        :key="person.name"
        class="pa-5"
      >
        <v-card
          class="bg-white rounded-t-xl pb-5"
          border="primary md"
          flat
        >
          <img
            :src="person.image"
            class="w-100 rounded-t-xl"
          >
          <div class="mt-3 text-body-1">
            {{ person.name }}
          </div>
          <div class="mt-3 text-grey-lighten-1 font-italic text-body-1">
            {{ person.title }}
          </div>
          <div class="mt-5 text-grey-darken-1 mx-5">
            {{ person.description }}
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-sheet>
</template>

<script setup>
const team = [
  {
    image: "./assets/team/person1.png",
    name: "CHRISTINA HAWKINS",
    title: "Head of SEO",
    description:
      "Johnathan is our co-founder and has developed search strategies for a variety of clients for over 5 years.",
  },
  {
    image: "./assets/team/person2.png",
    name: "CHRISTINA HAWKINS",
    title: "Head of SEO",
    description:
      "Johnathan is our co-founder and has developed search strategies for a variety of clients for over 5 years.",
  },
  {
    image: "./assets/team/person3.png",
    name: "CHRISTINA HAWKINS",
    title: "Head of SEO",
    description:
      "Johnathan is our co-founder and has developed search strategies for a variety of clients for over 5 years.",
  },
];
</script>
