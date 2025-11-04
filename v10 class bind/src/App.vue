<script>
export default{
    data(){
        return {
            isActive : false,
            hasError : true,
            classObject : {
                bg: true,
                'text-danger': true
            },
            bgClass : 'bg',
            erClass : 'text-danger'
        }

    }
}
</script>

<template>
    <div class="border" :class="{'bg' : isActive, 'text-danger' : hasError}">Warning</div>
    <div class="border" :class="classObject">Warning</div>
    <div class="border" :class="[bgClass, erClass]">Warning</div>
    <div class="border" :class="[isActive ? bgClass : '', erClass]">Warning</div>
    
</template>

<style>
.border {border: 2px solid red;}
.bg {background-color: gray;}
.text-danger {color: red;}
</style>
