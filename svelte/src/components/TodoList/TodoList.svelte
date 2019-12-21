<script>
    import Swal from 'sweetalert2';
    import TodoItem from './TodoItem.svelte';
    $: todos = [];
    async function add(){
        const { value: text } = await Swal.fire({
            title: 'Add Todo',
            input: 'text',
            inputPlaceholder: 'Enter Name of Todo'
        });
        if(text) todos = [...todos, text];
    }
</script>

<style>
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

<div id="todo-list">
    {#each todos as todo}
        <TodoItem content={todo} />
    {/each}
    <div class="todo-user--add" on:click={add}>
        <div class="todo-content todo-content--add"> add an item </div>
    </div>
</div>