<script>
export default{
    props : ["name", "age"],
    created(){
        console.log(this.name);
    },
    methods : {
        propsUpdate(){
            this.age = 30;
        }
    }
}
</script>

<template>
    <h1>Child component</h1>
    <p>Name : {{ name }}</p>
    <p>Age : {{ age }}</p>
    <button @click="propsUpdate">버튼</button>
    <!-- 해당 버튼 클릭시 에러 -->
</template>