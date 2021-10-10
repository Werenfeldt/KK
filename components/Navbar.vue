<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      color="#fcb69f"
      dark
      shrink-on-scroll
      :src="require('@/assets/img/sky.png')"
      scroll-target="#scrolling-techniques-2"
    >
      <v-app-bar-nav-icon class="black--text"></v-app-bar-nav-icon>

      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(46, 49, 49, .5), rgba(183, 28, 28, .5)"
        ></v-img>
      </template>
      <v-spacer></v-spacer>

      <v-avatar size="200px" tile>
        <v-img :src="require('@/assets/img/MrKite.png')" contain> </v-img>
      </v-avatar>
      <v-spacer></v-spacer>

      <v-app-bar-title class="black--text"> KiteKlang Audio</v-app-bar-title>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>

      <v-spacer></v-spacer>
      <v-btn icon class="black--text">
        <v-icon>mdi-instagram</v-icon>
      </v-btn>
      <v-btn icon class="black--text">
        <v-icon>mdi-facebook</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs centered>
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

<style>
.v-app-bar-title {
  font-size: 250% !important;
}
</style>
