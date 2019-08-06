<template>
    <div>
        <form @submit="addTodo">
            <input type="text" v-model="title" name="title" placeholder="Add a todo...">
            <input type="submit" value="Submit" class="btn">
        </form>
    </div>
</template>

<script>

export default {
    name: "AddTodo",

    data() {
        return {
            title: ''
        }
    },

    methods: {
        //Catch a new Todo
        addTodo(e){
            e.preventDefault();
            const newTodo = {
                title: this.title,
                completed: false
            }
            //Send Todo to Parent
            this.$emit('add-todo', newTodo);
            this.title = '';
        }
    }
}
</script>

<style scoped>
    form {
        display: flex;
    }
    input[type="text"]{
        flex: 10;
        padding: 5px;
        border: 0;
    }
    input[type="button"]{
        flex: 2;
    }
</style>
