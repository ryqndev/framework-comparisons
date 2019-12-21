<template>
    <div class="todo-item" v-on:click="toggle">
        <div class="todo-content"  v-bind:class="{ 'todo-complete': complete }"> {{content}} </div>
        <div class="todo-check"> {{complete ? "⦿" : "◯"}} </div>
    </div>
</template>

<script>
	export default {
        name: "TodoItem",
        props: ['content'],
		data: () => ({
			complete: false
        }),
        methods: {
            toggle: function(){
                this.complete = !this.complete   
            }
        }
	};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
