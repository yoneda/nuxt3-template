<template>
    <p class="test">this is sample text</p>
    <p>this is sample text too :{{ testValue }}</p>
    <p>this is counter :{{ count }}</p>
    <p>this is component name :{{ name }}</p>
    <button @click="testFunc">click me</button>
    <button @click="$emit('updateGlobalCount')">update global count</button>
</template>

<script>
// 通常のVue3-optionsAPIでのコンポーネントの書き方
export default {
    props: ['name'],
    emits: ['updateGlobalCount'],
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

// Vue3-optionsAPIでのvue-facing-decoratorを使ったクラス記法っぽい書き方
// import { Component, Vue } from 'vue-facing-decorator'
// @Component
// export default class Counter extends Vue{
//     count = 0
//     testValue = "hey, smith"

//     testFunc(){
//         this.count++
//     }
// }


</script>

<style>
    .test{
        background-color: red;
    }
</style>