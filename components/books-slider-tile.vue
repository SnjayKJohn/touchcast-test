<template>
	<v-slide-item v-slot="{}" class="books-slider-tile">
		<v-card
			:color="'black lighten-1'"
			class="ma-4"
			@click="$emit('book-selected', book)"
			width="230"
		>
			<v-img class="white--text align-end" :src="imgUrl" height="100%">
				<div>
					<v-card-title class="books__title-3 ma-0">{{ book.title }}</v-card-title>
					<v-card-text>
						<p class="books__text-2 mb-1">{{ book.author }}</p>
						<p class="books__text-3 ma-0">{{ book.publisher }}</p>
					</v-card-text>
				</div>
			</v-img>
		</v-card>
	</v-slide-item>
</template>

<script>
export default {
	props: {
		book: {
			default: {}
		},
		imgUrl: { default: '' }
	},

	mounted() {
		this.$parent.$emit('book-selected', this.book);
	}
};
</script>

<style lang="scss">
.books-slider-tile {
	&:hover {
		transform: scale(1.08);
	}
	.v-responsive__sizer {
		background-image: linear-gradient(to top, black, transparent);
	}
}
</style>
