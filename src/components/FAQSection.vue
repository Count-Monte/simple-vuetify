<template>
  <v-sheet
    class="text-center"
    height="700px"
  >
    <div class="text-h4 font-weight-medium mt-15 text-blue-grey-darken-4">
      Frequently Asked Questions
    </div>
    <div class="text-body-1 text-grey-darken-1 mt-5">
      Quis autem velis ets reprehender net etid quiste voluptate
    </div>
    <v-row class="pa-10 text-left">
      <v-col
        v-for="n in 4"
        :key="n"
        cols="6"
        class="pa-10"
      >
        <div class="text-h6 font-weight-bold text-blue-grey-darken-2">
          Velit ut tortizi pretium viverra suspendisse?
        </div>
        <div class="text-body-1 text-grey-darken-1 mt-5">
          Utise wisi enim minim veniam, quis et stationes ullamcorper nets
          suscipit ets lobotis nisle consequat nihis etim. Quis autem velis ets
          reprehender net etid quiste voluptate velitte esse sedis.
        </div>
      </v-col>
    </v-row>
  </v-sheet>
</template>
