<template>
    <p class="test">this is sample text</p>
    <p>this is sample text too {{ testValue }}</p>
    <p>this is counter {{ count }}</p>
    <button @click="testFunc">click me</button>
</template>

<script>
export default {
    data: () => ({
        count: 0,
        testValue: "hey, tarou"
    }),
    methods:{
        testFunc(){
            this.count++
        }
    }
}
</script>

<style>
    .test{
        background-color: red;
    }
</style>