<script>
export default{
    props : ["toDoList"],
    
}
</script>

<template>
    <ul id="todo-list">
        <li v-for="(item, i) in toDoList" :class="item.done ? 'completed' : ''">
            {{ item.toDo }}
            <!-- <button type="button" @click="$emit('delete', i)">Delete</button> -->
            <button type="button" @click="$emit('completeToDo', i)">Delete</button>
        </li>
    </ul>
</template>