<script>
    export let content;
    let toggle = () => {

    }
    let complete = true;
</script>

<style>
    .todo-item {
        display: grid;
        grid-template-columns: 1fr 50px;
        padding: 10px;
    }
    .todo-check {
        text-align: right;
    }
    .todo-complete {
        color: grey;
    }
</style>

<div class="todo-item" on:click={toggle}>
    <div class="todo-content {complete && "todo-complete"}"> {content} </div>
    <div class="todo-check"> {complete ? "⦿" : "◯"} </div>
</div>