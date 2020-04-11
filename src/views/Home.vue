<template>
	<div
		class="bg-gray-1000 min-h-screen flex justify-center align-center flex-col"
	>
		<div class="flex justify-center align-center pb-32">
			<img src="@/assets/logo.gif" alt="logo" class="h-72" />
		</div>
		<div class="bg-black flex justify-center">
			<div class="flex flex-col w-1/4 py-48">
				<p class="text-white text-md text-center break-words px-16 pb-12">
					We Believe That Everyone Should Have A Spot To Safely Store Their
					Passwords With No Worries At All.
				</p>
				<button
					class="bg-yellow-1000 hover:bg-gray-1000 text-black hover:text-yellow-1000 font-bold py-2 px-6 rounded-full mx-24"
				>
					About
				</button>
			</div>
			<div class="flex flex-col w-1/4 py-48">
				<p class="text-white text-md text-center break-words px-16 pb-12">
					With The Combination Of High Security, And Great Developers, LockIt
					Offers You The Best Password Managing App
				</p>
				<button
					class="bg-yellow-1000 hover:bg-gray-1000 text-black hover:text-yellow-1000 font-bold py-2 px-6 rounded-full mx-24"
				>
					Download
				</button>
			</div>
			<div class="flex flex-col w-1/4 py-48">
				<p class="text-white text-md text-center break-words px-16 pb-12">
					Are You Interested In Joining A Team With A New Set Of Challenges And
					Communicate With Professionals?
				</p>
				<button
					class="bg-yellow-1000 hover:bg-gray-1000 text-black hover:text-yellow-1000 font-bold py-2 px-6 rounded-full mx-24"
				>
					Open Jobs
				</button>
			</div>
		</div>
		<div
			class="bg-gray-1000 text-yellow-1000 flex flex-col justify-center align-center min-h-1/3 w-screen mb-24 text-6xl team mt-12"
		>
			<p class="mb-12 text-center">The Team</p>
			<div class="flex justify-center align-center flex-wrap">
				<div
					v-for="person in team"
					:key="person.id"
					class="max-w-sm rounded shadow-3xl mx-4 p-4 center w-1/6"
				>
					<img
						class="w-24 h-24 rounded-half"
						:src="person.imageURL"
						:alt="person.name"
					/>
					<div class="px-6 py-4">
						<div class="font-bold text-xl mb-2 text-white">
							{{ person.name }}
						</div>
						<p class="text-sm">
							{{ person.title }}
						</p>
					</div>
				</div>
			</div>
		</div>
		<div class="bg-gray-1100 py-24 flex justify-center align-center">
			<vue-typed-js
				:strings="testimonials"
				:typeSpeed="50"
				:backSpeed="50"
				loop
				:backDelay="1000"
				:cursorChar="'_'"
				smartBackspace
				class="text-white text-2xl"
			>
				<h1 class="typing"></h1>
			</vue-typed-js>
		</div>
	</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Home extends Vue {
	team = [
		{
			id: 1,
			name: 'Jorge Zapata',
			title: 'CEO/iOS Developer',
			imageURL: require('@/assets/JorgeZapata.png')
		},
		{
			id: 2,
			name: 'Audrick Ong',
			title: 'CTO/Full Stack Developer',
			imageURL: require('@/assets/Ricky.png')
		},
		{
			id: 3,
			name: 'Solomon O.',
			title: 'Android Developer',
			imageURL: require('@/assets/solomon.png')
		},
		{
			id: 4,
			name: 'Pavan Rajput',
			title: 'Android Developer',
			imageURL: require('@/assets/Pavan.png')
		}
	];
	testimonials = [
		'Nice dark-mode feel!',
		'The safest you can be!',
		'As safe as a bunker!'
	];
}
</script>

<style scoped>
button {
	text-transform: uppercase;
	font-weight: 500;
	letter-spacing: 1px;
}
.team {
	font-family: 'Montserrat', sans-serif;
}
.center {
	text-align: -webkit-center;
}
.wrapper {
	background-color: #051e3e;
	height: 100vh;
	color: white;
	display: flex;
	justify-content: center;
	align-items: center;
}
</style>
