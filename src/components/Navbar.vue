<template>
	<nav class="flex items-center justify-center flex-wrap bg-gray-1000 p-6">
		<div class="flex items-center flex-shrink-0 text-white mr-6">
			<img src="@/assets/logo.png" alt="LockIt! logo" class="max-w-xxs" />
		</div>
		<div class="w-full block flex-grow flex items-center">
			<div class="text-sm flex-grow flex justify-center">
				<router-link
					to="#"
					class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-24"
					>Company</router-link
				>
				<router-link
					to="#"
					class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-24"
					>About</router-link
				>
				<router-link
					to="#"
					class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-24"
					>Download</router-link
				>
				<router-link
					to="#"
					class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-24"
					>Contact</router-link
				>
				<router-link
					to="#"
					class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-24"
					>Jobs</router-link
				>
			</div>
		</div>
	</nav>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Navbar extends Vue {}
</script>

<style scoped>
* {
	font-family: 'Baloo Paaji 2' cursive;
	text-transform: uppercase;
}
.navbar-start {
	display: flex;
	align-items: center;
	width: 100vw;
}
</style>
