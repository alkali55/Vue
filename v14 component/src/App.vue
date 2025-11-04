<script>
import GlobalChild from './components/GlobalChild.vue';
import LocalComponent from './components/LocalChild.vue';

export default{
    components: {
        LocalComponent,

    }
}
</script>

<template>
    <h1>App.vue</h1>
    <LocalComponent></LocalComponent>
    <GlobalChild></GlobalChild>
</template>

<style>
</style>
