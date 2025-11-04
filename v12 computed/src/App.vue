<script>
export default{
    data() {
        return {
            chk : false,
            firstName : "John",
            lastName : "Doe"
        }
    },
    computed: {
            yesNo(){
                if(this.chk){
                    return "예";
                } else {
                    return "아니오";
                }
            },
            fullName : {
                get(){
                    return this.firstName + ' ' + this.lastName;
                },
                set(newValue){
                    const names = newValue.split(' ');
                    this.firstName = names[0];
                    this.lastName = names[names.length - 1];
                }
            }
    }
}
</script>

<template>
    <input type="checkbox" v-model="chk">{{ chk }}
    <input type="checkbox" v-model="chk">{{ yesNo }}

    <div>
        <p>full Name: {{ fullName }}</p>
        <input v-model="fullName" placeholder="Enter full name">
        firstName : {{ firstName }} <br>
        lastName : {{ lastName }}

    </div>
</template>

<style>
</style>
