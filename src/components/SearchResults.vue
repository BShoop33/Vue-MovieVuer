<template>
  <div>
    <v-sheet
      v-if="searchResults"
      elevation="1"
      class="mx-auto"
      max-width="1000"
    >
      <h3 class="pl-5 mt-5">
        Found {{ searchResults.total_results }} results for "{{ searchTerm }}"
      </h3>
      <v-slide-group class="pb-5" show-arrows>
        <!-- <v-slide-item v-for="movie in searchResults.results" :key="movie.id"> -->
        <v-slide-item v-for="movie in viewableMovies" :key="movie.id">
          <!-- <v-img
            contain
            :src="`https://image.tmdb.org/t/p/w200${movie.poster_path}`"
            height="200"
            width="150"
          ></v-img> -->
          <v-img
            @click="selectMovie(movie)"
            contain
            :src="`https://image.tmdb.org/t/p/w200${movie.poster_path}`"
            height="200"
            width="150"
          ></v-img>
        </v-slide-item>
      </v-slide-group>
    </v-sheet>
  </div>
</template>

<script>
import { mapState, mapGetters, mapActions } from "vuex";

export default {
  computed: {
    ...mapState(["searchResults", "searchTerm"]),
    ...mapGetters(["viewableMovies"]),
  },
  methods: {
    ...mapActions(["selectMovie"]),
  },
};
</script>

<style>
</style>