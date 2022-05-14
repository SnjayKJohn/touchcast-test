<template>
  <v-slide-item v-slot="{ active, toggle }" class="books-slider-tile">
    <v-card
      :color="active ? 'primary' : 'grey lighten-1'"
      class="ma-4"
      :height="height"
      :width="250"
      @click="toggle"
    >
      <v-row class="fill-height" align="center" justify="center">
        <v-scale-transition>
          <v-icon
            v-if="active"
            color="white"
            size="48"
            v-text="'mdi-close-circle-outline'"
          ></v-icon>
        </v-scale-transition>
      </v-row>
    </v-card>
  </v-slide-item>
</template>

<script>
export default {
  props: {
    book: {
      default: {},
    },
  },
  data() {
    return {
      height: 300,
      width: 500,
      scale: 50,
    }
  },
}
</script>

<style lang="scss" scoped>
.books-slider-tile:hover {
  transform: scale(
    1.05
  ); /* (150% zoom - Note: if the zoom is too large, it will go outside of the viewport) */
}
</style>
