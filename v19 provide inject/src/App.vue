<script>
import FisrtChild from './components/FisrtChild.vue';
export default{
    components : {
        FisrtChild
    },
    data(){
        return {
            gift : "장난감"
        }
    },
    provide(){
        return{
            gift : this.gift
        }
    }
}
</script>

<template>
    <div>
        <h1>부모 컴포넌트입니다.</h1>
        <FisrtChild></FisrtChild>
    </div>
</template>

<style scoped>

</style>
