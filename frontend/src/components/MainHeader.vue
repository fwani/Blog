<template>
  <v-app-bar class="text-white" :elevation="2" color="#323232FF">
    <v-btn>HOME</v-btn>
    <v-btn>BLOG</v-btn>
    <v-btn>ABOUT</v-btn>
    <v-spacer></v-spacer>
    <v-card
        class="mx-auto text-white"
        color="#323232FF"
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
</template>

<script>
export default {
  name: "MainHeader",

  data: () => ({
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