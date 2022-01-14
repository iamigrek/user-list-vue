<template>
	<button>
		<slot></slot>
	</button>
</template>

<script>
export default {
	name: 'my-button'
}
</script>

<style scoped>
	button {
		padding: 10px;
		border: 2px solid teal;
		background-color: transparent;
		color: teal;
		cursor: pointer;
	}
</style>