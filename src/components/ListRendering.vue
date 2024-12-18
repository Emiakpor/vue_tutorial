<template>

    <input v-model="newTodo" placeholder="new todo"/> &nbsp
    <button @click="addTodo">Add todo</button>
    <br>
    <ul>
        <li v-for="todo in todos" :key="todo.id"> 
            {{ todo.text }}
            <button @click="removeTodo(todo)"> X </button>
        </li>
    </ul>
</template>

<script setup lang="ts">
    import { ref } from  'vue';

    let id = 0;
    const newTodo = ref('');
    const todos = ref([
        { id: id++, text: 'Learn HTML' },
        { id: id++, text: 'Learn JavaScript' },
        { id: id++, text: 'Learn CSS' },
        { id: id++, text: 'Learn Vue' },
    ]);



    function addTodo() {
        todos.value.push({id: id++, text: newTodo.value});
        newTodo.value = ''
    }

    function removeTodo(todo:object) {
        todos.value = todos.value.filter(t => t !== todo)
    }
</script>

<style scoped>

</style>