<script>

  export default {
    data(){
      return {
        channel : "<b>Vue 기초학습</b>",
        subscribe : 2677,
      }
    }
  }

</script>

<template>

  <p>채널명 : {{ channel }}</p>
  <p>구독 : {{ subscribe }}</p>
  <p>{{ "오늘의 행운 숫자 " + Math.ceil(Math.random() * 45) }}</p>
  <p v-html="channel"></p>
  <p v-text="channel"></p>
  <p v-text="subscribe"></p>
  <p v-pre>채널명 : {{ channel }}</p>

</template>

<style>
</style>
