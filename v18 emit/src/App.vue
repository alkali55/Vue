<script>
import LocalChild from './components/LocalChild.vue';
export default{
    data(){
        return {
            c: 0
        }
    },
    components : {
        LocalChild
    },
    methods : {
        callFunction(var1){
            console.log("자식 컴포넌트에서 보낸 이벤트 수신" + var1);
            this.c = var1
        }
    }
}
</script>

<template>
    <h1>나는 부모 컴포넌트 ({{ c }})</h1>

    <LocalChild @create-post="callFunction"></LocalChild>

</template>

<style>
</style>
