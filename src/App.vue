<template>
	<div class="app">
		<user-add 
			@create="createUser"/>
		<user-list 
			:users="users"
			@remove="removeUser"
			/>
	</div>
</template>

<script>
import UserAdd from '@/components/UserAdd.vue'
import UserList from '@/components/UserList.vue'

export default {
	components: {
		UserAdd, UserList
	},
	data() {
		return {
			users: [
				{id: 1, name: 'User1'},
				{id: 2, name: 'User2'},
				{id: 3, name: 'User3'},
			]
		}
	},
	methods: {
		createUser(user) {
			this.users.push(user)
		},
		removeUser(user) {
			this.users = this.users.filter(u => u.id !== user.id)
		}
	}
}
</script>

<style>
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	.app {
		max-width: 600px;
		margin: 0 auto;
		padding: 30px 15px;
	}
</style>