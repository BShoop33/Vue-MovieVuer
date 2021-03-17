<template>
  <v-app>
    <v-app-bar app color="green darken-2" dark> </v-app-bar>

    <v-main>
      <v-container>
        <search-results />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import SearchResults from "./components/SearchResults";

export default {
  components: {
    SearchResults,
  },

  data: () => ({
    //
  }),
};
</script>
