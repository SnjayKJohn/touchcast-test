<template>
  <div>
    <main-section />
    <books-slider />
  </div>
</template>

<script>
import BooksSlider from '~/components/books-slider.vue'
import mainSection from '~/components/main-section.vue'
export default {
  components: { mainSection, BooksSlider },
}
</script>

<style></style>
