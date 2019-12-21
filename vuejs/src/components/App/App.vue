<template>
	<div id="app">
		<Header />
		<TodoList />
	</div>
</template>

<script>
import Header from '../Header/Header.vue'
import TodoList from '../TodoList/TodoList.vue'

export default {
	name: 'app',
	components: {
		Header,
		TodoList
	}
}
</script>

<style>
	body{
		margin: 0;
		color: white;
		font-family: 'Lato', sans-serif;
		background-color: #272727;
	}
	#app {
		max-width: 450px;
		margin: 0 auto;
	}
</style>
