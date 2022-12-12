<template>
        <!-- 能够把里面的标签传送给指定标签的最后的位置 -->
        <Teleport to=".app">
                <p>这是一个P标签</p>
        </Teleport>
<p>子组件</p>
<slot name="link"></slot>
<slot  name="btn"  :myNum="num"></slot>
</template>

<script lang='ts' setup>
import Table from '@/components/HelloWorld.vue'
import {  ref } from 'vue' 
        let num=ref(20)
</script>
 
<style lang= "less" scoped>
    
</style>