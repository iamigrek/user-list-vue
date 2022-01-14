<template>
	<ul class="list">
		<user-list-item 
			v-for="user in users" 
			:user="user" 
			:key="user.id"
			@remove="$emit('remove', user)"
			/>
	</ul>
</template>

<script>
import UserListItem from '@/components/UserListItem.vue'

export default {
	components: {
		UserListItem
	},
	props: {
		users: {
			type: Array,
			required: true
		}
	}
}
</script>

<style>
	.list {
		list-style: none;
		padding: 0;
		margin: 0;
		border: 2px solid teal;
		padding: 10px;
		border-radius: 10px;
	}
	
</style>