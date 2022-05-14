<template>
	<v-menu
		content-class="mt-5 px-6"
		right
		:close-on-content-click="false"
		absolute
		min-width="300"
	>
		<template v-slot:activator="{ on, attrs }">
			<v-btn
				icon
				text
				:ripple="false"
				v-show="attrs"
				style="position: absolute; right: 20px"
				class="text-h5"
				v-bind="attrs"
				v-on="on"
				@click="$emit('close')"
			>
				<v-img :src="search" height="20" contain />
			</v-btn>
		</template>
		<v-text-field full-width label="Search..."></v-text-field>
	</v-menu>
</template>

<script>
import search from '../assets/img/search.png';
export default {
	data() {
		return {
			search
		};
	}
};
</script>

<style></style>
