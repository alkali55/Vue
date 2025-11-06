<script>
import ToDoInput from './components/ToDoInput.vue';
import ToDoList from './components/ToDoList.vue';
export default{
    components : {
        ToDoInput,
        ToDoList
    },
    data(){
        return{
            toDoList : [],
        }
    },
    methods : {
        saveInput(toDoInput){
            this.toDoList.push({toDo : toDoInput, done : false});
        },
        // deleteTodo(i){
        //     this.toDoList.splice(i, 1);
        // }
        completeToDo(i){
            this.toDoList[i].done = true;
            // console.log(this.toDoList);
        }
    }
}
</script>

<template>

    <div class="todo-container">
        <h1>TODO List</h1>

        <ToDoInput @input-submit="saveInput">
 
        </ToDoInput>


        <!-- <ToDoList :toDoList @delete="deleteTodo">

        </ToDoList> -->

        <ToDoList :toDoList @complete-to-do="completeToDo">

        </ToDoList>
    </div>
</template>
