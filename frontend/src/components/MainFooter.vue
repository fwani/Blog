<template>
  <v-footer class="d-flex flex-column">
    <v-container fluid style="color: white; background-color: #323232FF">
      <v-row justify="center" style="padding-bottom: 50px; font-size: 24px">
        <v-col cols="6"><strong>Get connected with me on social networks!</strong></v-col>
        <v-spacer></v-spacer>
        <v-col cols="4">
          <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-2"
              :icon="icon"
              variant="plain"
              size="default"
          ></v-btn>
        </v-col>
      </v-row>
      <v-row align-content="center">
        <v-col align-self="end">Designed by Fwani in Seoul, 2022</v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  name: "MainFooter",

  data: () => ({
    icons: [
      'mdi-facebook',
      'mdi-twitter',
      'mdi-linkedin',
      'mdi-instagram',
    ],
  }),
}
</script>

<style scoped>

</style>