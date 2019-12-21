<template>
	<div id="todo-list">
        <TodoItem v-for="todo of todos" v-bind:key="todo" v-bind:content="todo" />
        <div class="todo-user--add" v-on:click="add">
            <div class="todo-content todo-content--add"> add an item </div>
        </div>
    </div>
</template>

<script>
    import Swal from 'sweetalert2';
    import TodoItem from './TodoItem.vue';

	export default {
        name: "TodoList",
        components: {
            TodoItem
        },
		data: () => ({
			todos: []
        }),
        methods: {
            add: async function(){
                const { value: text } = await Swal.fire({
                    title: 'Add Todo',
                    input: 'text',
                    inputPlaceholder: 'Enter Name of Todo'
                });
                if(text) this.todos.push(text);
            }
        }
	};
	</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    #todo-list {
        padding: 0 40px 40px 40px;
        height: calc(100vh - 200px);
        /* overflow-y: scroll; */
    }
    .todo-user--add {
        color: grey;
        padding: 7px 0 10px 0;
        margin: 20px 10px 5px 10px;
        border: 2px dashed grey;
        border-radius: 20px;
        transition: color 350ms, border-color 350ms;
    }
    .todo-user--add:hover,
    .todo-user--add:active {
        color: white;
        border-color: #FF00FF;
    }
    .todo-content--add {
        text-align: center;
    }
</style>
