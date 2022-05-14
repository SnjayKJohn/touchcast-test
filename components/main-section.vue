<template>
  <div>
    <v-img :src="bg">
      <row>
        <v-col cols="12" md="6">
          <h2 class="books__title-1">Bookshelf & Book Racks</h2>
          <p class="books__text-1">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat.
          </p>
        </v-col>
      </row>
    </v-img>
  </div>
</template>

<script>
import bg from '../assets/img/bg.jpg'
export default {
  data() {
    return {
      bg,
    }
  },
}
</script>

<style></style>
