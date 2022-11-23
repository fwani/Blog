<template>
  <v-app>
    <v-main>
      <v-carousel :show-arrows="false"
                  :continuous="false"
                  hide-delimiter-background
                  delimiter-icon="mdi-square"
                  height="700">
        <v-carousel-item :src="require('../assets/jirisan.jpeg')" cover>
          <div class="d-flex fill-height justify-center align-center">
            <div class="w-66 pa-5" style="background-color: #323232FF; color: white">
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
  }),
}
</script>

<style scoped>

</style>