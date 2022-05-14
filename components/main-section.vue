<template>
	<div>
		<v-img :src="bg">
			<v-row class="ma-0">
				<v-col cols="10" md="4" class="ma-md-16 ma-4 pt-16">
					<h2 class="books__title-1">Bookshelf & Book Racks</h2>
					<p class="books__text-1">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
						tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
						veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
						commodo consequat.
					</p>
				</v-col>
			</v-row>
			<div class="my-10">
				<h4 class="books__title-2 mx-16 my-4">Hardcover Fiction</h4>
				<books-slider />
			</div>
		</v-img>
	</div>
</template>

<script>
import bg from '../assets/img/bg.jpg';
import booksSlider from './books-slider.vue';
export default {
	components: { booksSlider },
	data() {
		return {
			bg
		};
	}
};
</script>

<style></style>
