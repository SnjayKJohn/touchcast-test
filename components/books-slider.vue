<template>
  <v-sheet class="mx-auto transparent" elevation="8">
    <v-slide-group v-model="model" class="pa-0" center-active show-arrows>
      <books-slider-tile v-for="n in 15" :key="n" :book="n" />
    </v-slide-group>
  </v-sheet>
</template>

<script>
import booksSliderTile from './books-slider-tile.vue'
export default {
  components: { booksSliderTile },
  data: () => ({
    model: null,
  }),
}
</script>

<style></style>
