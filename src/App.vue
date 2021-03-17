<template>
  <v-app>
    <v-app-bar app color="green darken-2" dark> </v-app-bar>

    <v-main>
      <v-container>
        <app-header />
        <search-results />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import SearchResults from "./components/SearchResults";
import AppHeader from "./components/AppHeader";

export default {
  components: {
    SearchResults,
    AppHeader,
  },

  data: () => ({
    //
  }),
};
</script>
