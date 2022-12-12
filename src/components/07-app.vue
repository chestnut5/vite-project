<template>
    <Child>
<!-- 插槽的使用 -->
        <template v-slot:link>
            <a href="#">a标签</a>
        </template>
        <!-- scope插槽作用域 -->
        <template #btn="scope">
            <button>按钮{{scope.myNum}}</button>
        </template>

    </Child>
</template>

<script lang='ts' setup>
import Child from './07-appChild.vue'
import {   } from 'vue' 
       console.log(globalVar,globalObj);
        fn()
</script>
 
<style lang= "less" scoped>
    
</style>