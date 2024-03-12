<template>
  <v-container class="fill-height">
    <v-responsive class="mx-auto rounded-lg" max-width="800" style="background-color: #2B2D31;">
      <v-card class="p-3 rounded-none">
        <div class="flex flex-row justify-between gap-5">
          <div class="flex flex-row gap-2 align-center">
            <div>
              <span class="i-iconoir-check-circle-solid text-4xl text-green" />
            </div>
            <div>
              <h5 class="text-grey">Your Welcome Screen is up and running.</h5>
              <h5 class="text-grey">New members will be greeted by this screen when they join!</h5>
            </div>
          </div>
          <div class="flex flex-row align-center gap-2">
            <v-btn text class="shadow-none">Preview</v-btn>
            <v-btn color="#a7121d" dark>Disable</v-btn>
          </div>
        </div>
      </v-card>

      <div class="flex flex-col align-center mt-[20px]">
        <div class="logo">
          <v-img height="50" width="55" src="@/assets/logo.png" />
        </div>
        <div class="text-h6 font-weight-light mb-n1">Welcome to <b class="text-h6 font-weight-bold">Vuetify</b></div>
        <div class="background-text">A community for Vue and Vuetify developers. Vuetify is a free Open Source Vue
          Component Framework<span>43</span></div>
      </div>

      <v-divider class="my-[20px] mx-[20px]" />

      <div class="px-[20px] pb-[20px]">
        <div>
          <h5 class="text-grey mb-[5px]">TOP THINGS TO DO</h5>
          <h5 class="text-grey">Select up to 5 recommended channels. We suggest channels where people can interact, like
            channels for
            discussions, asking questions, reading news, or selecting roles.</h5>
        </div>

        <v-row class="mt-[10px]">
          <list-item v-for="item in list" :key="item.title" :data="item" />
        </v-row>
      </div>
    </v-responsive>
  </v-container>
</template>

<script setup>
const list = [{
  class: 'i-iconoir-car',
  title: 'Introduce yourself to the Community',
  channel: '# introductions'
}, {
  class: 'i-iconoir-cylinder',
  title: 'Ask general questions about Vuetify',
  channel: '# general-discussion'
}, {
  class: 'i-iconoir-paste-clipboard',
  title: 'Get help & advice direct from Vuetify pros',
  channel: '# subscriber-help'
}, {
  class: 'i-iconoir-cinema-old',
  title: 'Obtain community assistance for Vuetify 3',
  channel: '# vuetify-3-help'
}, {
  class: 'i-iconoir-report-columns',
  title: 'Obtain community assistance for Vuetify 2',
  channel: '# vuetify-2-help'
}]
</script>

<style scoped>
.logo {
  background-color: #1D1E22;
  width: fit-content;
  border-radius: 10px;
  padding: 5px 2px 2px 2px;
}

.background-text {
  width: 60%;
  text-align: center;
  background-color: #25262A;
  color: #717477;
  padding: 10px;
  border-radius: 10px;
  margin-top: 10px;
  position: relative;

  span {
    position: absolute;
    right: 10px;
    bottom: 10px;
    color: #919497;
    font-size: 13px;
  }
}
</style>
