<template>
  <v-sheet
    color="#E52F37"
    height="650px"
    class="ga-10 text-center pt-15"
  >
    <div class="text-white text-h4 font-weight-medium">
      Contact Us
    </div>
    <div class="text-center text-body-1">
      Have any queries? Get in touch today.
    </div>
    <v-row class="ma-0 px-15 mt-10">
      <v-col cols="6">
        <v-text-field
          bg-color="transparent"
          single-line
          variant="outlined"
          hide-details
          flat
          label="Your Name*"
        />
      </v-col>
      <v-col cols="6">
        <v-text-field
          bg-color="transparent"
          single-line
          hide-details
          variant="outlined"
          flat
          label="Email Address*"
        />
      </v-col>
      <v-col cols="6">
        <v-text-field
          bg-color="transparent"
          single-line
          hide-details
          variant="outlined"
          flat
          label="Phone Number*"
        />
      </v-col>
      <v-col cols="6">
        <v-text-field
          bg-color="transparent"
          single-line
          hide-details
          variant="outlined"
          flat
          label="Option*"
        />
      </v-col>
      <v-col cols="12">
        <v-textarea
          bg-color="transparent"
          lines="4"
          hide-details
          variant="outlined"
          flat
          label="Your Message..."
        />
      </v-col>
    </v-row>
    <v-btn
      class="ml-5 text-red-lighten-1 px-10 text-body-1"
      height="55px"
      flat
    >
      GET IN TOUCH
    </v-btn>
  </v-sheet>
</template>
