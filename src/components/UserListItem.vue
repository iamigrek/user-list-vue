<template>
	<li class="list__item">
			<h3 class="title">{{ user.name }}</h3>
			<my-button 
				@click="$emit('remove', user)"
				>delete</my-button>
		</li>
</template>

<script>
export default {
	props: {
		user: {
			type: Object,
			required: true
		}
	}
}
</script>

<style>
	.list__item {
		border: 2px solid teal;
		padding: 10px;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
	.list__item:not(:last-child) {
		margin-bottom: 20px;
	}
	.title {
		color: teal;
	}
</style>