<template>
	<v-row class="mx-md-16 pa-md-10 pa-4">
		<v-col cols="12" md="4">
			<h2 class="books__title-4 text-left mb-8">{{ book.title }}</h2>
			<v-img
				class="white--text align-end mb-6"
				:src="imgUrl"
				width="60"
				style="border-radius: 4px"
			>
			</v-img>
			<v-btn class="text-none px-10"> Add to favourites + </v-btn>
		</v-col>
		<v-col cols="12" md="6" class="ml-md-16">
			<h4 class="books__title-3 mb-1 text-left">{{ book.author }}</h4>
			<p class="books__text-4 mb-10 text-left">{{ book.publisher }}</p>
			<p class="books__text-5 text-left pa-0">{{ book.description }}</p>
		</v-col>
		<v-btn
			icon
			style="position: absolute; right: 20px"
			class="text-h5"
			@click="$emit('close')"
		>
			<v-img height="20" contain :src="close" />
		</v-btn>
	</v-row>
</template>

<script>
import close from '../assets/img/close.png';
export default {
	props: {
		book: {
			default: {}
		},
		imgUrl: { default: '' }
	},
	data() {
		return {
			close
		};
	}
};
</script>

<style></style>
