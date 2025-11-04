<script>

  export default {
    data(){
      return {
        sports: [
          'Baseball',
          'Football',
          'Volleyball',
          'Swimming',
        ],
        count : 0,

      }
    }
  }

</script>

<template>

  <ul>
    <li v-for="item in sports">{{ item }}</li>
    <li v-for="(item, index) in sports">{{ index }} {{ item }}</li>
  </ul>

  <p>{{ "count : " + count }}</p>
  <button v-on:click="count++">숫자 증가</button>
  <button v-on:click="count--">숫자 감소</button>
  <button v-on:mouseover="count=0">초기화</button>

</template>

<style>
</style>
