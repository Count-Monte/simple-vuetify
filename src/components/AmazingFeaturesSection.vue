<template>
  <v-sheet
    class="text-center"
    height="500px"
  >
    <div class="text-h4 font-weight-medium mt-15 text-blue-grey-darken-4">
      Amazing Features
    </div>
    <div class="text-body-1 text-grey-darken-1 mt-5">
      Quis autem velis ets reprehender net etid quiste voluptate.
    </div>
    <v-row class="pa-10">
      <v-col
        v-for="item in features"
        :key="item.title"
        cols="4"
        class="d-flex ga-5 pa-5 text-left"
      >
        <div class="mt-2">
          <img :src="item.icon">
        </div>
        <div>
          <div class="text-h6 font-weight-bold text-blue-grey-darken-4">
            {{ item.title }}
          </div>
          <div class="text-body-1 text-grey-darken-1 mt-2">
            {{ item.description }}
          </div>
        </div>
      </v-col>
    </v-row>
  </v-sheet>
</template>

<script setup>
const features = [
  {
    icon: './assets/features/support.png',
    title: 'Support 24/7',
    description:
      'Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.'
  },
  {
    icon: './assets/features/user.png',
    title: 'User Friendly',
    description:
      'Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.'
  },
  {
    icon: './assets/features/bell.png',
    title: 'Notifications',
    description:
      'Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.'
  },
  {
    icon: './assets/features/accessibility.png',
    title: 'Accessibility',
    description:
      'Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.'
  },
  {
    icon: './assets/features/control.png',
    title: 'Control',
    description:
      'Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.'
  },
  {
    icon: './assets/features/chat.png',
    title: 'Chat With Friends',
    description:
      'Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.'
  }
]
</script>
