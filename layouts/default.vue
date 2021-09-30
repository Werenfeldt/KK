<template>
  <v-app>
    <Navbar />
    <v-sheet
      id="scrolling-techniques-2"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 1000px">
        <Nuxt />
      </v-container>
    </v-sheet>
    <Footer />
  </v-app>
</template>

<script>
export default {}
</script>
