<script>

  export default {
    data(){
      return {
        score : 75,
        isTrue : true,
        subscribe : 2677,
      }
    }
  }

</script>

<template>

  <h1 v-if="score >= 90">평점 : A</h1>
  <h1 v-else-if="score >= 80">평점 : B</h1>
  <h1 v-else-if="score >= 70">평점 : C</h1>
  <h1 v-else-if="score >= 60">평점 : D</h1>
  <h1 v-else>평점 : F</h1>

  <h1 v-show="isTrue">v-show에서 처리하는 영역</h1>
  <h1 v-show="!isTrue">v-show에서 처리하는 영역</h1>

</template>

<style>
</style>
