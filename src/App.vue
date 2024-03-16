<template>
  <v-app theme="light" style="max-width: 1200px" class="ma-auto">
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
            >{{ item }}</v-btn
          >
        </div>
      </template>
    </v-toolbar>
    <div>
      <v-sheet
        color="#860A0A"
        class="d-flex flex-column align-center justify-center"
        height="600px"
      >
        <div class="text-h3 mt-10 font-weight-medium">
          Welcome To Landing Page
        </div>
        <div class="text-h6 mt-5 font-weight-light w-50 text-center">
          Exceptru sentum occaecat cupidatat nonet proident, vante nislat
          quistamused officituames ets deserunt etimus nets.
        </div>
        <div class="mt-3 d-flex align-center justify-center mb-10 w-50">
          <v-text-field
            base-color="transparent"
            single-line
            hide-details
            rounded
            variant="solo"
            label="Enter Your Email Address"
          />
          <v-btn class="ml-5" height="55px" rounded color="#E52F37" flat
            >GET STARTED</v-btn
          >
        </div>
      </v-sheet>
      <v-sheet class="d-flex align-center justify-center py-15 ga-5">
        <img v-for="item in banners" :key="item" :src="item" />
      </v-sheet>
      <v-sheet color="#F1FAFF" class="py-15 text-center" height="500px">
        <div class="text-h4 font-weight-bold">What We Do</div>
        <div class="text-body-1 font-weight-regular mt-3 text-grey-darken-2">
          Discover how our amazing team can help your business.
        </div>
        <v-row class="ma-5">
          <v-col
            v-for="item in whatWeDo"
            :key="item.title"
            class="d-flex flex-column align-center"
          >
            <img :src="item.icon" />
            <div class="text-h6 mt-1">{{ item.title }}</div>
            <div class="text-body-1 mt-2 text-grey-darken-2 w-75">
              {{ item.description }}
            </div>
          </v-col>
        </v-row>
      </v-sheet>
      <v-sheet
        class="d-flex flex-row align-center justify-space-around"
        height="500px"
      >
        <div>
          <img src="./assets/discover_bg.png" />
        </div>
        <div class="w-50">
          <div class="text-h4">
            Discover how we can help you to group your business fast
          </div>
          <div class="text-body-1 text-grey-darken-1 my-5">
            Venis demo enim ipsam voluptatem quia voluptas sit aspernatur netsum
            lorem fugit, seditum netis velas matrix net nesciunt
          </div>
          <div
            class="text-grey-darken-1 my-2"
            v-for="text in discover_text"
            :key="text"
          >
            <v-icon icon="mdi-check-bold" color="red" end />
            {{ text }}
          </div>
          <v-btn class="ml-5" height="55px" rounded color="#E52F37" flat
            >Discover More</v-btn
          >
        </div>
      </v-sheet>
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
              <img :src="item.icon" />
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
          <img src="./assets/customize_bg.png" class="elevation-5" />
        </div>
      </v-sheet>
      <v-sheet color="#E52F37" height="450px" class="text-center px-15 pt-15">
        <div class="text-h3 font-weight-bold mb-5">
          Fun Facts About Our Agency
        </div>
        <v-row class="mx-15">
          <v-col class="mt-10" v-for="item in agency" :key="item.title">
            <img :src="item.icon" />
            <div class="text-h4 font-weight-bold mt-5">{{ item.title }}</div>
            <div class="text-body-1 mt-5">{{ item.description }}</div>
          </v-col>
        </v-row>
      </v-sheet>
      <v-sheet color="#F1FAFF">
        <v-row class="pa-10 d-flex align-center">
          <v-col class="pa-15">
            <div class="text-h4 font-weight-medium">
              What People Are Saying.
            </div>
            <div class="text-body-1 text-grey-darken-1 mt-5">
              Quis autem velis ets reprehender net etid quiste nets voluptate.
              Utise wisi enim minim venim, quis etsad aspernatis netsum
              stationes nets.
            </div>
            <v-row class="mt-5">
              <div v-for="(item, index) in ['TrustPilot', 'Feefo']" :key="item">
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
                    ></v-icon>
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
                <img src="./assets/avatar.png" />
                <div class="font-weight-bold text-blue-grey-darken-4 text-h6">
                  John Done /
                  <span class="text-green-lighten-1">CEO - Epic Design</span>
                </div>
              </div>
            </v-alert>
          </v-col>
        </v-row>
      </v-sheet>
      <v-sheet class="text-center pt-15" height="900px">
        <div class="text-h4 font-weight-bold">Our Portfolio</div>
        <div class="text-body-1 text-grey-darken-1 mt-5">
          Discover the latest projects accomplished for my clients.
        </div>
        <v-row class="mt-5 ga-7 pa-10" style="height: 600px">
          <v-col class="d-flex flex-column align-between ga-7">
            <v-row class="h-50 bg-grey-lighten-1"></v-row>
            <v-row class="h-50 bg-grey-lighten-1"></v-row>
          </v-col>
          <v-col class="bg-grey-lighten-1"></v-col>
          <v-col class="d-flex flex-column align-between ga-7">
            <v-row class="h-30 bg-grey-lighten-1"></v-row>
            <v-row class="h-30 bg-grey-lighten-1"></v-row>
            <v-row class="h-30 bg-grey-lighten-1"></v-row>
          </v-col>
        </v-row>
      </v-sheet>
      <v-sheet class="text-center pt-20" height="800px" color="#F1FAFF">
        <div class="text-h4 font-weight-bold">Meet Our Team</div>
        <div class="text-body-1 text-grey-darken-1 mt-5">
          Discover more about our high performing team.
        </div>
        <v-row class="pa-10">
          <v-col v-for="person in team" :key="person.name" class="pa-5">
            <v-card class="bg-white rounded-t-xl pb-5" border="primary md" flat>
              <img :src="person.image" class="w-100 rounded-t-xl" />
              <div class="mt-3 text-body-1">{{ person.name }}</div>
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
      <v-sheet
        color="#E52F37"
        height="400px"
        class="d-flex flex-column align-center justify-center"
      >
        <div class="text-white text-h4 font-weight-medium">
          Award-Winning Agency
        </div>
        <div class="mt-7 text-center">
          Utise wisi enim miim ennam, quis at straioines ullamcorper nets
          suspicit<br />
          ets lobot.js risle consequant hihis etim aspernatur netsum.,
        </div>
        <div class="w-50 d-flex justify-space-around mt-15">
          <v-btn
            class="ml-5 text-red-darken-2 text-body-2"
            height="55px"
            rounded
            flat
            >Discover Mode</v-btn
          >
          <v-btn
            class="ml-5 text-white text-body-2 bg-red-darken-3"
            height="55px"
            rounded
            color="#E52F37"
            flat
            >Get In Touch</v-btn
          >
        </div>
      </v-sheet>
      <v-sheet class="text-center" height="500px">
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
              <img :src="item.icon" />
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
      <v-sheet class="d-flex align-center pa-15" height="600px" color="#F1FAFF">
        <v-row class="d-flex align-center">
          <v-col cols="5">
            <div class="text-h4 font-weight-bold text-blue-grey-darken-2">
              Great pricing plans tailored to your needs.
            </div>
            <div class="text-body-1 text-grey-darken-1 mt-5">
              Quis autem velis ets reprehender net etid quiste voluptate. Utise
              wisi enim minim veniam, quis et stationes nets.
            </div>
          </v-col>
          <v-col cols="3">
            <v-card
              class="pt-10 pb-5 rounded-0 d-flex flex-column align-center justify-center ga-5 elevation-5"
            >
              <div class="text-h6 font-weight-bold">MONTHLY</div>
              <div class="text-h2 font-weight-bold">$19</div>
              <div class="text-body-1 text-grey-darken-1">Per Month</div>
              <v-btn
                class="text-body-1 text-red-darken-1 font-weight-bold"
                flat
              >
                GET STARTED
              </v-btn>
              <div class="text-center text-body-1 text-grey-darken-1">
                First two weeks free. <br />
                Amazing features.
              </div>
            </v-card>
          </v-col>
          <v-col cols="4" class="px-5">
            <v-card
              class="pt-10 pb-5 rounded-0 d-flex flex-column align-center justify-center ga-10 bg-red-darken-1 rounded elevation-5"
            >
              <div class="text-h6 font-weight-bold">ANNUALY</div>
              <div class="text-h2 font-weight-bold">$29</div>
              <div class="text-body-1 text-white">Per Month</div>
              <v-btn
                class="ml-5 text-red-lighten-1 px-10 text-body-1"
                height="55px"
                flat
                rounded
                >GET IN TOUCH</v-btn
              >
              <div class="text-center text-body-1 text-white">
                First two weeks free. <br />
                Save 45% with this plan<br />Amazing features.
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-sheet>
      <v-sheet class="text-center" height="700px">
        <div class="text-h4 font-weight-medium mt-15 text-blue-grey-darken-4">
          Frequently Asked Questions
        </div>
        <div class="text-body-1 text-grey-darken-1 mt-5">
          Quis autem velis ets reprehender net etid quiste voluptate
        </div>
        <v-row class="pa-10 text-left">
          <v-col v-for="n in 4" :key="n" cols="6" class="pa-10">
            <div class="text-h6 font-weight-bold text-blue-grey-darken-2">
              Velit ut tortizi pretium viverra suspendisse?
            </div>
            <div class="text-body-1 text-grey-darken-1 mt-5">
              Utise wisi enim minim veniam, quis et stationes ullamcorper nets
              suscipit ets lobotis nisle consequat nihis etim. Quis autem velis
              ets reprehender net etid quiste voluptate velitte esse sedis.
            </div>
          </v-col>
        </v-row>
      </v-sheet>
      <v-sheet color="#E52F37" height="650px" class="ga-10 text-center pt-15">
        <div class="text-white text-h4 font-weight-medium">Contact Us</div>
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
          >GET IN TOUCH</v-btn
        >
      </v-sheet>
      <v-footer class="pa-8">
        <div class="text-body-1">
          2021 <b>Landing Page</b>. Designed by Christopher Saburo
        </div>
      </v-footer>
    </div>
  </v-app>
</template>

<script setup>
const menu = [
  "Home",
  "About",
  "Testimonals",
  "Work",
  "Team",
  "Features",
  "Pricing",
];
const features = [
  {
    icon: "./assets/features/support.png",
    title: "Support 24/7",
    description:
      "Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.",
  },
  {
    icon: "./assets/features/user.png",
    title: "User Friendly",
    description:
      "Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.",
  },
  {
    icon: "./assets/features/bell.png",
    title: "Notifications",
    description:
      "Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.",
  },
  {
    icon: "./assets/features/accessibility.png",
    title: "Accessibility",
    description:
      "Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.",
  },
  {
    icon: "./assets/features/control.png",
    title: "Control",
    description:
      "Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.",
  },
  {
    icon: "./assets/features/chat.png",
    title: "Chat With Friends",
    description:
      "Utise wisi enim minim veniam, quis tation ullamcorper suscipit et loboti nisl consequat nihis.",
  },
];
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
const banners = [
  "./assets/banner/csswinner.png",
  "./assets/banner/cssawards.png",
  "./assets/banner/fwa.png",
  "./assets/banner/cssdesignawards.png",
];
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
];
const agency = [
  {
    icon: "./assets/agency/completed.png",
    title: "1050+",
    description: "Projects Completed",
  },
  {
    icon: "./assets/agency/heart.png",
    title: "217k",
    description: "Happy Clients",
  },
  {
    icon: "./assets/agency/awards.png",
    title: "1210",
    description: "Design Awards",
  },
  {
    icon: "./assets/agency/anchor.png",
    title: "2137",
    description: "Line Of Codes",
  },
];
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
const discover_text = [
  "Quias netus magni netsum eos qui ratione sequi",
  "Venis ratione sequi netus enim quia tempor magne",
  "Venis ratione sequi netus enim quia tempor magne",
];
</script>
