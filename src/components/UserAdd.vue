<template>
	<form @submit.prevent class="form">
		<input class="from__input" type="text" placeholder="Username" v-model="user.name">
		<my-button 
			@click="createUser"
			class="form__btn"
			>add</my-button>
	</form>
</template>

<script>

export default {
	data() {
		return {
			
		user: {
				name: ''
			}
		}
	},
	methods: {
		createUser() {
			this.user.id = Date.now();
			this.$emit('create', this.user)
			this.user = {
				name: ''
			}
			
		}
	}
}
</script>

<style>
	.form {
		display: flex;
		margin-bottom: 20px;
	}

	.from__input {
		padding: 10px;
		border: 2px solid teal;
		background-color: transparent;
		color: teal;
		margin-right: 10px;
		width: 100%;
	}
</style>