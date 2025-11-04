<script>
export default{
    data(){
        return{
            kValue : ""
        }
    }
    ,
    methods : {
        getKey(e){
            // this.kValue = e.key;
            alert("alt+s");
        },
        createAlert(){
            
                alert("경고장이 떴습니다.");
        }
    }
}
</script>

<template>
    <button v-on:click.once="createAlert">클릭해 보세요.</button>
    <input type="text" v-on:keydown="getKey">
    <input type="text" v-on:keydown.alt.s="getKey">
    <!-- .enter .tab .delete .esc .space .up .down .left .right .center -->
    <span>{{ kValue }}</span>
</template>

<style>
</style>
