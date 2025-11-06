<script>
export default{
    props : ["buttonName"],
    data(){
        return {
            buttonName : "잘가",
        }
    }
}
</script>

<template>
    <button class="fancy-btn">
        <slot name="btn1"></slot>
    </button>

    <button class="fancy-btn">
        <slot name="btn2">디폴트 값</slot>
    </button>

</template>