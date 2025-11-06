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
        <slot :buttonName></slot>
    </button>
</template>