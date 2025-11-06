<script>
import FancyButton from './components/FancyButton.vue';
import MainLayout from './components/MainLayout.vue';
import NewButton from './components/NewButton.vue';
export default {
    components : {
        FancyButton,
        MainLayout,
        NewButton
    },
    data(){
        return{
            buttonName : "클릭클릭",

        }
    }
}
</script>

<template>
    <h1>나는 App.vue</h1>

    <MainLayout>
        <template v-slot:header>
            <h1>Header</h1>
        </template>
        <template v-slot:contents>
            <h1>Contents</h1>
        </template>
        <template #footer>
            <!--  v-slot:을 #으로 축약가능  -->
            <h1>Footer</h1>
        </template>
        <template #default>
            <h1>Default</h1>
        </template>
    </MainLayout>


    <FancyButton>
        <template #btn1>{{buttonName}}</template>
        <template #btn2></template>
    </FancyButton>

    <NewButton v-slot="props">
        {{ props.buttonName }}
    </NewButton>
    
    <NewButton v-slot="{buttonName}">
        {{ buttonName }}
    </NewButton>
</template>

<style>
</style>
