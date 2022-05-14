<template>
	<v-sheet class="mx-auto transparent" elevation="8">
		<v-slide-group v-model="model" class="pa-0" center-active show-arrows>
			<books-slider-tile
				v-for="(book, index) in books"
				:key="index"
				:book="book"
				:imgUrl="getImgUrl(book)"
				@book-selected="bookSelected"
			/>
			<template v-slot:next>
				<v-btn icon height="60" width="60">
					<v-img :src="sliderArrow" height="40" contain />
				</v-btn>
			</template>
			<template v-slot:prev>
				<v-btn icon height="60" width="60" style="transform: rotateY(180deg)">
					<v-img :src="sliderArrow" height="40" contain />
				</v-btn>
			</template>
		</v-slide-group>
		<v-bottom-sheet v-model="bottomSheet">
			<v-sheet v-if="selectedBook">
				<book-detail
					:book="selectedBook"
					:imgUrl="getImgUrl(selectedBook)"
					@close="bottomSheet = false"
				/>
			</v-sheet>
		</v-bottom-sheet>
	</v-sheet>
</template>

<script>
import booksSliderTile from './books-slider-tile.vue';
import sliderArrow from '../assets/img/slider_arrow.png';
import { mapState } from 'vuex';
import BookDetail from './book-detail.vue';
export default {
	components: { booksSliderTile, BookDetail },
	data: () => ({
		model: null,
		bottomSheet: false,
		selectedBook: {},
		sliderArrow
	}),
	computed: {
		...mapState(['books'])
	},
	methods: {
		getImgUrl(book) {
			if (book.book_image) return require('@/assets/img/books/' + book.book_image);
		},
		bookSelected(book) {
			this.selectedBook = book;
			this.bottomSheet = true;
		}
	}
};
</script>

<style></style>
