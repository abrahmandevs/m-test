<script setup>
	import { ref, defineProps, defineEmits } from "vue"
	const props = defineProps({
		message: String,
	})
	const emit = defineEmits(["messageEmitted"])

	/* function eventMessageEmitted() {
		emit("messageEmitted", "from child components")
	} */
</script>

<template>
	<div>
		<h2 class="font-semibold text-gray-700">{{ message }}</h2>
		<button @click="$emit('messageEmitted', `${message} from child components`)" class="inline-block m-5 px-4 py-2 text-white bg-emerald-600 hover:bg-emerald-600/80 border-0 rounded-lg shadow-emerald-700/60 shadow-lg transition-all duration-300 outline-none focus:outline-none">Click Me</button>
		<!-- <button @click="eventMessageEmitted" class="px-4 py-2 text-white bg-emerald-600 hover:bg-emerald-600/80 border-0 rounded-lg shadow-emerald-700/60 shadow-lg transition-all duration-300 outline-none focus:outline-none">Click Me</button> -->
	</div>
</template>

<style scoped></style>
