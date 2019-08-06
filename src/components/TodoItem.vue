<template>
    <div class="todo-item" v-bind:class="{'is-completed':todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{ todo.title }}
            <button @click="$emit('del-todo', todo.id)" class="del">X</button>
        </p>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        markComplete(){
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>

<style scoped>

    .todo-item {
        background-color: #f4f4f4;
        padding: 10px;
        border-bottom: 1px solid dotted;
    }

    .is-completed {
        text-decoration: line-through;
    }

    .del {
        background-color: #ff0000;
        border: none;
        color: #fff;
        padding: 5px 9px;
        border-radius: 50%;
        cursor: pointer;
        float: rigth;
    }
</style>
