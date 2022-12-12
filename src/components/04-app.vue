<template>
    <p>{{num}}</p>
</template>


<script setup lang="ts">
//setup 语法糖加上之后 script之间的代码会被Vue内部自动添加到原先的setup语法上ß
import {reactive,toRefs} from 'vue'
let obj={
    num:12
}

let objRef=reactive(obj)
let {num}=toRefs(objRef)


</script>