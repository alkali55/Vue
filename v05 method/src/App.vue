<script>

export default{
    data(){
        return {
            userName : "김길중",
            num : 0,
        }

    },
    methods : {
        increment(){
            this.num++
        },
        decrement(){
            this.num--
        },
        greeting(userName) {
            return "Hi, there " + userName
        }
    }
}
</script>

<template>
    <h1>{{ greeting("asdf") }}</h1>
    <p>{{ num }}</p>
    <button v-on:click="increment">Increse number</button>
    <button v-on:click="decrement">Decrese number</button>
</template>

<style>
</style>
