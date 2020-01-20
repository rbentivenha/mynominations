<template>
  <v-app dark>
    <v-app-bar fixed app>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <template v-slot:extension>
        <v-tabs align-with-title background-color="transparent">
          <v-tab to="/">Mapa</v-tab>
          <v-tab to="/poi">POI</v-tab>
        </v-tabs>
      </template>
    </v-app-bar>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer app>
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      title: "Pokestops"
    };
  }
};
</script>
