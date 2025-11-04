<script>
export default {
    data(){
        return {
            myWidth : '400px',
            myWidthTwo : 10


        }
    },
    methods : {
        incWidth : function(){
            this.myWidthTwo += 10;
        },
        initWidth : function(){
            this.myWidthTwo = 10;
        }
    }
}
</script>

<template>
    <div class="demo" v-bind:style="{width: '300px', height: '500px'}"></div>
    <div class="demo" :style="{width: myWidth, height: '500px'}"></div>
    <!-- v-bind 생략가능 -->
    <div class="demo" @mouseover="initWidth" v-bind:style="{width: myWidthTwo + 'px', height: '500px'}"></div>
    <button @click="incWidth">버튼을 클릭해보세요.</button>
</template>

<style>
    .demo {
        width: 100px;
        height: 100px;
        background-color: blueviolet;
    }
</style>
