<template>
	<div class="col-span-x">
		<ContentSlot />
	</div>
</template>

<script setup lang="ts">
const { width } = defineProps({
	width: {
		type: Number,
		default: 1,
	},
});
</script>

<style scoped>
.col-span-x {
	grid-column: span v-bind(width) / span v-bind(width);
}
</style>
