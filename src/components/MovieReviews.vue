<template>
  <div v-if="reviews && reviews.length > 0">
    <h3 class="red--text">User Reviews</h3>
    <ul>
      <li v-for="review in reviews" :key="review.id">
        <p>{{ review.author_details.avatar_path }}</p>
        <p>{{ review.author }}</p>
        <div class="my-2">
          <v-icon>mdi-calendar</v-icon>
          Created {{ formatDate(review.created_at) }}
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import { mapState } from "vuex";
import { dateMixin } from "../mixins/movieMixins";

export default {
  mixins: [dateMixin],
  computed: {
    ...mapState(["reviews"]),
  },
};
</script>