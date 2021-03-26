<template>
  <v-app>
    <app-header />
    <v-main>
      <v-container>
        <search-results />
        <v-row class="mt-6">
          <v-col :sm="12" :md="6">
            <movie-details />
          </v-col>
          <v-col :sm="12" :md="6">
            <movie-reviews />
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>

  <!-- <v-card v-if="movieDetails">
    <v-img
      :src="`https://image.tmdb.org/t/p/w500${movieDetails.backdrop_path}`"
    ></v-img>
    <v-card-title color="red">{{ movieDetails.title }}</v-card-title>
    <v-card-subtitle>
      <div>
        <v-icon>mdi-clock</v-icon>
        {{ movieDetails.runtime }} mins
      </div>
      <div class="mt-2">
        <v-icon>mdi-calendar</v-icon>
        Released {{ movieDetails.release_date }}
      </div>
    </v-card-subtitle>
    <v-card-text>
      {{ movieDetails.overview }}
      <div class="mt-3">
        <v-chip
          class="mr-1"
          v-for="genre in movieDetails.genres"
          :key="genre.id"
        >
          {{ genre.name }}
        </v-chip>
      </div>
    </v-card-text>
  </v-card> -->
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import MovieDetails from "./components/MovieDetails";
import MovieReviews from "./components/MovieReviews";
import SearchResults from "./components/SearchResults";

export default {
  components: {
    SearchResults,
    AppHeader,
    MovieDetails,
    MovieReviews,
  },
};
</script>