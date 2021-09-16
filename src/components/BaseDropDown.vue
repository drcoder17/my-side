<template>
	<div class="dropdown w-28" @click="hovered = !hovered">
		<div class="list flex items-center bg-gray-400 cursor-pointer">
			<span class="fas fa-globe pb-1 pr-2"></span>
			<span class="font-mono">{{ selected ? selected : defText }}</span>
		</div>
		<div
			class="list-items cursor-pointer bg-gray-200 inline-block mb-1 border-2 pl-1"
			:class="{ 'show-me': hovered }"
			@click="selectItem(item)"
			v-for="item in items"
			:key="item"
		>
			{{ item }}
		</div>
		<!-- //TODO => paste code in the below to use this basic dropdown -->
		<!-- <base-dropdown
			:items="items"
			:defText="defText"
			v-on:selItem="selectedItem"
		/> -->
	</div>
</template>

<script>
	export default {
		data() {
			return {
				selected: '',
				hovered: false,
				//TODO => send items Array and defText via props to use this basic dropdown
				items: ['Arabia', 'Bosnia', 'Cairo'],
				defText: 'Cities',
			};
		},
		//TODO => uncomment code in the below to use this basic dropdown
		// props: {
		// 	items: {
		// 		type: Array,
		// 		required: true,
		// 	},
		// 	defText: {
		// 		type: String,
		// 		required: true,
		// 	},
		// },
		methods: {
			//TODO paste v-on:selectItem event get value
			selectItem(item) {
				this.selected = item;
				this.$emit('selItem', item);
			},
		},
	};
</script>

<style scoped>
	.list-items {
		display: none;
	}
	.show-me {
		display: block;
	}
</style>
