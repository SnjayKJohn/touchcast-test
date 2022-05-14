<template>
	<v-app dark>
		<v-app-bar :clipped-left="clipped" fixed app flat class="transparent">
			<logo />
			<v-spacer />
			<search />
		</v-app-bar>
		<v-main class="pt-0">
			<Nuxt />
		</v-main>
	</v-app>
</template>

<script>
import logo from '~/components/logo.vue';
import Search from '~/components/search.vue';
export default {
	components: { logo, Search },
	data() {
		return {
			clipped: false
		};
	}
};
</script>
