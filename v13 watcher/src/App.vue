<script>
export default{
    data(){
        return {
            count : 0,
            y : "짝수"
        }
    },
    methods : {
        increment(){
            this.count++;
        }
    },
    watch: {

        // count(newVal, oldVal){
        //     console.log(`Count Changed from ${oldVal} to ${newVal}`);
        //     if(newVal % 2 === 0){
        //         this.y = "짝수";
        //     } else {
        //         this.y = "홀수";
        //     }
        // }
        
        count : {
            handler(newVal, oldVal){
                console.log(`Count Changed from ${oldVal} to ${newVal}`);
                if(newVal % 2 === 0){
                    this.y = "짝수";
                } else {
                    this.y = "홀수";
                }
            },
            once : true
        }
    }
}
</script>

<template>
    <div>
        <p>count : {{ count }}</p>
        <button @click="increment">Increment</button>
        <p>Result : {{ y }}</p>
    </div>
</template>

<style>
</style>
