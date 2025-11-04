<script>
export default{
    inject: ["gift"]
}
</script>

<template>
    <div>
        <h1>손자 컴포넌트입니다.</h1>
        <p>물려받은 것 : {{ gift }}</p>
    </div>
</template>

<style scoped>

</style>