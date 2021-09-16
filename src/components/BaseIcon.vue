<template>
	<i class="icon flex items-center">
		<div class="mr-3">
			<slot name="text" class="text"></slot>
		</div>
		<div>
			<slot name="icon" class="icon"></slot>
		</div>
	</i>
</template>

<script>
	export default {
		name: 'BaseIcon',
	};
</script>
