<template>
  <v-app
    theme="light"
    style="max-width: 1200px"
    class="ma-auto"
  >
    <v-toolbar class="pl-5">
      <template #prepend>
        <div class="text-h4 font-weight-bold my-5 red text-red-darken-2">
          Landing Page
        </div>
      </template>

      <template #append>
        <div class="hidden-sm-and-down">
          <v-btn
            v-for="item in menu"
            :key="item"
            variant="text"
            class="text-body-1 blue-grey-darken-4"
          >
            {{ item }}
          </v-btn>
        </div>
      </template>
    </v-toolbar>

    <LandingSection />
    <LogoSection />
    <WhatWeDoSection />
    <DiscoverHelp />
    <CustomizeSection />
    <FunFactsSection />
    <WhatPeopleSaySection />
    <OurPortfolioSection />
    <MeetOurTeamSection />
    <AwardWinningSection />
    <AmazingFeaturesSection />
    <PricingSection />
    <FAQSection />
    <ContactUsSection />

    <v-footer class="pa-8">
      <div class="text-body-1">
        2021 <b>Landing Page</b>. Designed by Christopher Saburo
      </div>
    </v-footer>
  </v-app>
</template>

<script setup>
import AmazingFeaturesSection from './components/AmazingFeaturesSection.vue';
import AwardWinningSection from './components/AwardWinningSection.vue';
import ContactUsSection from './components/ContactUsSection.vue';
import CustomizeSection from './components/CustomizeSection.vue';
import DiscoverHelp from './components/DiscoverHelp.vue';
import FAQSection from './components/FAQSection.vue';
import FunFactsSection from './components/FunFactsSection.vue';
import MeetOurTeamSection from './components/MeetOurTeamSection.vue';
import OurPortfolioSection from './components/OurPortfolioSection.vue';
import PricingSection from './components/PricingSection.vue';
import WhatPeopleSaySection from './components/WhatPeopleSaySection.vue';
import WhatWeDoSection from './components/WhatWeDoSection.vue';

const menu = [
  "Home",
  "About",
  "Testimonals",
  "Work",
  "Team",
  "Features",
  "Pricing",
];

</script>
