<script>
	import Header from '../Header/Header.svelte';
	import TodoList from '../TodoList/TodoList.svelte';
</script>

<style>
	:global(body){
		margin: 0;
		color: white;
		font-family: 'Lato', sans-serif;
		background-color: #272727;
	}
	.app {
		max-width: 450px;
		margin: 0 auto;
	}
</style>

<div class="app">
	<Header />
	<TodoList />
</div>
