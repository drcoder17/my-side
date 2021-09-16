<template>
	<button class="rounded-3xl shadow-lg py-3 px-6 font-bold font-mono">
		<slot name="content"></slot>
	</button>
</template>

<script>
	export default {
		name: 'BaseBtn',
	};
</script>
