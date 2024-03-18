<template>
  <v-sheet color="#F1FAFF">
    <v-row class="pa-10 d-flex align-center">
      <v-col class="pa-15">
        <div class="text-h4 font-weight-medium">
          What People Are Saying.
        </div>
        <div class="text-body-1 text-grey-darken-1 mt-5">
          Quis autem velis ets reprehender net etid quiste nets voluptate. Utise
          wisi enim minim venim, quis etsad aspernatis netsum stationes nets.
        </div>
        <v-row class="mt-5">
          <div
            v-for="(item, index) in ['TrustPilot', 'Feefo']"
            :key="item"
          >
            <v-alert
              :border="index === 1 ? 'start' : 'none'"
              border-color="grey"
              class="pt-3 bg-transparent rounded-0"
            >
              <div class="font-weight-bold text-blue-grey-darken-4">
                {{ item }}
              </div>
              <div>
                <v-icon
                  v-for="n in 5"
                  :key="n"
                  class="text-yellow-darken-2 ml-0"
                  icon="mdi-star"
                  end
                />
              </div>
            </v-alert>
          </div>
        </v-row>
      </v-col>
      <v-col>
        <v-alert
          v-for="n in 3"
          :key="n"
          class="my-5 elevation-5 bg-white rounded-0"
          border="start"
          border-color="#27b36a"
          outlined
        >
          <div class="d-flex flex-row align-center ga-3">
            <img src="../assets/avatar.png">
            <div class="font-weight-bold text-blue-grey-darken-4 text-h6">
              John Done /
              <span class="text-green-lighten-1">CEO - Epic Design</span>
            </div>
          </div>
        </v-alert>
      </v-col>
    </v-row>
  </v-sheet>
</template>
