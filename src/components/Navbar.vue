<template>
	<div class="sitenav">
		<base-dropdown
			:items="items"
			:defText="defText"
			v-on:selItem="selectedItem"
		/>
	</div>
</template>

<script>
	import BaseDropDown from './BaseDropDown.vue';
	export default {
		name: 'Navbar',
		data() {
			return {
				items: ['A', 'B', 'C'],
				defText: 'skills',
			};
		},
		components: {
			'base-dropdown': BaseDropDown,
		},
		methods: {
			selectedItem(i) {
				console.log(i);
			},
		},
	};
</script>

<style scoped></style>
