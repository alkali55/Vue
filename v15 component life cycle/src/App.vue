<script>
import GlobalChild from './components/GlobalChild.vue';

export default{
    data(){
        return{
            cnt : 1
        }
    },
    beforeCreate(){ console.log("beforeCreated"); },
    created(){ console.log("created"); },
    beforeMount(){ console.log("beforeMount"); },
    mounted(){ console.log("mounted"); },
    beforeUpdate(){ console.log("beforeUpdate"); },
    updated(){ console.log("updated"); },
    beforeUnmount(){ console.log("beforeUnmount"); },
    unmounted(){ console.log("unmounted"); },
    methods : {
        counter(){
            this.cnt++;
        },
        disCounter(){
            this.cnt--;
        }
    }
}
</script>

<template>
    <h1>App.Vue</h1>
    <h1>Count : {{ cnt }}</h1>
    <GlobalChild v-if="cnt == 2"></GlobalChild>
    <button @click="counter">Count + 1</button>
    <button @click="disCounter">Count - 1</button>
</template>

<style>
</style>
