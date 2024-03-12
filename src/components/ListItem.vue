<template>
  <v-col cols="12" class="p-1">
    <v-card class="pa-2 bg-[#313338] shadow-none">
      <v-card-text class="p-1">
        <div class="flex items-center justify-between">
          <div class="flex items-center gap-2">
            <div class="rounded-full w-10 h-10 flex items-center justify-center text-white text-center p-2">
              <span class="text-4xl text-white" :class="data.class" />
            </div>
            <div>
              <div class="font-bold text-black-500 text-center">
                {{ data.title }}
              </div>
              <span class="text-grey">
                {{ data.channel }}
              </span>
            </div>
          </div>
          <div>
            <v-btn text class="bg-[#404248] text-[#7B7C7F] shadow-none">Edit</v-btn>
          </div>
        </div>
      </v-card-text>
    </v-card>
  </v-col>
</template>

<script setup>
defineProps({ data: { type: Object, required: true } })
</script>
