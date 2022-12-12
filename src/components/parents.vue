<template>
    <!-- 父组件 -->
    <Child :num="num" @fn="chanNum"></Child>
</template>

<script lang='ts' setup>
import Child from './child.vue'
import {  ref } from 'vue' 
        let num=ref(20)

        const chanNum=(val:number)=>{
            num.value+=val
        }
</script>
 
<style lang= "less" scoped>
    
</style>