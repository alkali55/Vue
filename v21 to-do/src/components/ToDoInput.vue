<script>
export default{
    data(){
        return{
            toDoInput : "",
        }
    },
    methods : {
        submitInput(){
            this.$emit('inputSubmit' , this.toDoInput);
            this.toDoInput = "";
        }
    }
}
</script>

<template>
    <form id="todo-form">
            <input type="text" id="todo-input" placeholder="Enter a new task" v-model="toDoInput">
            <button type="button" @click="submitInput">Add</button>
            
    </form>
</template>