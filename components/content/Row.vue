<template>
	<div class="grid-cols-x">
		<ContentSlot />
	</div>
</template>

<script setup lang="ts">
const { columns } = defineProps({
	columns: {
		type: Number,
		default: 1,
	},
});
</script>

<style scoped>
.grid-cols-x {
	display: grid;
	grid-template-columns: repeat(calc(v-bind(columns)), minmax(0, 1fr));
}
</style>
