<script setup>
	import { ref } from "vue"
	import ChildComponent from "./ChildComponent.vue"

	// const parentMessage = ref("message from parent")
	const message = ref("message from parent")
	function receiveMessage(msg) {
		message.value = msg ?? ""
	}
</script>

<template>
	<div class="text-center space-y-3">
		<h2 class="text-xl font-semibold text-rose-500">{{ message }}</h2>
		<ChildComponent :message="message" @messageEmitted="receiveMessage" />
	</div>
</template>

<style scoped></style>

