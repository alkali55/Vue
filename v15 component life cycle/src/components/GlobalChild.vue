<script>

export default{
    beforeCreate(){ console.log("Global beforeCreated"); },
    created(){ console.log("Global created"); },
    beforeMount(){ console.log("Global beforeMount"); },
    mounted(){ console.log("Global mounted"); },
    beforeUpdate(){ console.log("Global beforeUpdate"); },
    updated(){ console.log("Global updated"); },
    beforeUnmount(){ console.log("Global beforeUnmount"); },
    unmounted(){ console.log("Global unmounted"); }
}

</script>

<template>
    <h1>전역 컴포넌트</h1>
    <p>전역 컴포넌트입니다.</p>
</template>

<style scoped>
h1 {color : red}
p {color : orangered}
</style>
