<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      color="#fcb69f"
      dark
      shrink-on-scroll
      src="https://picsum.photos/1920/1080?random"
      scroll-target="#scrolling-techniques-2"
    >
      <v-app-bar-nav-icon class="black--text"></v-app-bar-nav-icon>
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(213, 0, 0, .5), rgba(183, 28, 28, .5)"
        ></v-img>
      </template>
      <v-app-bar-title class="black--text">KiteKlang Audio</v-app-bar-title>
      <v-spacer></v-spacer>
      <v-btn icon class="black--text">
        <v-icon>mdi-instagram</v-icon>
      </v-btn>
      <v-btn icon class="black--text">
        <v-icon>mdi-facebook</v-icon>
      </v-btn>
      <template v-slot:extension>
        <v-tabs align-with-title>
          <v-tab class="black--text">Projects</v-tab>
          <v-tab class="black--text">Gear</v-tab>
          <v-tab class="black--text">Pricing</v-tab>
        </v-tabs>
      </template>
    </v-app-bar>
  </v-card>
</template>

<script>
export default {}
</script>

<style></style>
