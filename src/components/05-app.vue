<template>
    <!--watch 的写法 -->
    <p>{{num}}</p>
    <button @click="num++">按钮</button>
</template>

<script lang='ts' setup>
import { watch, ref ,toRefs,reactive} from 'vue'
// let num = ref(20)
// watch(num, (newVal, oldVal) => {
//     console.log(newVal, oldVal);

// })

let obj={
    num:30
}

let objRet=reactive(obj)
let {num }=toRefs(objRet)
watch(num,(newVal,oldVal)=>{
    console.log(newVal,oldVal)
    ;
    
})
</script>
 
<style lang= "less" scoped>
    
</style>