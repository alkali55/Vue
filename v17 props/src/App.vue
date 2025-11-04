<script>
import ChildCom from './components/ChildComponent.vue';
export default{
    data(){
      return{
        name : "John",
        age : 30,
      }

    },
    components: {
        ChildCom
    },
    methods : {
        ageInc(){
            this.age++;
        }
    }
}
</script>

<template>
    <h1>나는 부모</h1>
    <!-- <ChildCom name="홍길동" age="12"/> -->
     <button @click="ageInc">버튼</button>
    <ChildCom :name :age/>
</template>

<style>
</style>
