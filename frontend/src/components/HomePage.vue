<template>
  <v-app full-height>
    <v-app-bar class="text-white" :elevation="2" color="rgb(50,50,50)">
      <v-btn>HOME</v-btn>
      <v-btn>BLOG</v-btn>
      <v-btn>ABOUT</v-btn>
      <v-spacer></v-spacer>
      <v-card
          class="mx-auto text-white"
          color="rgb(50,50,50)"
          min-width="130"
          width="30%"
          max-width="300"
      >
        <v-card-text>
          <v-text-field
              :loading="loading"
              density="compact"
              variant="underlined"
              label="Search ..."
              append-inner-icon="mdi-magnify"
              single-line
              hide-details
              @click:append-inner="onClick"
          ></v-text-field>
        </v-card-text>
      </v-card>
    </v-app-bar>
    <v-main>
      <v-carousel :show-arrows="false"
                  :continuous="false"
                  hide-delimiter-background
                  delimiter-icon="mdi-square"
                  height="700">
        <v-carousel-item :src="require('../assets/jirisan.jpeg')" cover>
          <div class="d-flex fill-height justify-center align-center">
            <div class="w-66 pa-5" style="background-color: rgb(50,50,50); color: white">
              <h1 style="font-size: 70pt">Fwani's Blog</h1>
              <p style="font-size: 20pt">subject : normal, trip, code</p>
            </div>
          </div>
        </v-carousel-item>
      </v-carousel>

      <v-row no-gutters>
        <v-col cols="2"></v-col>
        <v-col cols="8">
          <v-row>
            <v-col v-for="c in 10" :key="c" cols="4">
              <PhotoCard/>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="2"></v-col>
      </v-row>
    </v-main>

    <v-footer app class="d-flex flex-column">
      <v-container fluid style="color: white; background-color: rgb(50,50,50)">
        <v-row justify="center" style="padding-bottom: 50px; font-size: 24px">
          <v-col><strong>Get connected with me on social networks!</strong></v-col>

          <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-2"
              :icon="icon"
              variant="plain"
              size="default"
          ></v-btn>
        </v-row>
        <v-row align-content="center">
          <v-col align-self="end">Designed by Fwani in Seoul, 2022</v-col>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
import PhotoCard from "@/components/PhotoCard";

export default {
  name: "HomePage",
  components: {
    PhotoCard,
  },
  data: () => ({
    icons: [
      'mdi-facebook',
      'mdi-twitter',
      'mdi-linkedin',
      'mdi-instagram',
    ],
    toggle: null,
    loaded: false,
    loading: false,
  }),
  methods: {
    onClick() {
      this.loading = true

      setTimeout(() => {
        this.loading = false
        this.loaded = true
      }, 2000)
    },
  },
}
</script>

<style scoped>

</style>