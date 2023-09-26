<template>
    <div id="app">
        <h1>Vue.js Slots Fundamentals</h1>
        <ToDoItem>
            Koop een bannaan
            <template #description>
                <p>Bananen zijn lekker</p>
            </template>
            <template #button-text>
                Make it noice
            </template>
        </ToDoItem>
        <ToDoItem>Peel a banana</ToDoItem>
        <ToDoItem>Eet een bannaan</ToDoItem>
    </div>
</template>

<script>
import ToDoItem from './components/ToDoItem.vue';

export default {
    components: {
        ToDoItem
    }
}
</script>

<style>
.done {
    color: green;
    text-decoration: line-through;
}
</style>