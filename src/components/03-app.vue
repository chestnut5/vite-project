<template>
    <p>{{num}}</p>
    <button @click="btnClick">按钮</button>
</template>
<script lang="ts">
import { defineComponent ,reactive,toRefs} from 'vue'
export default defineComponent({


    setup() {
let obj={
    num:25
}
// toRefs 的做 在解构reactive()里得到的对象的时候 他们解构成响应式数据
//解构出来的数据仍然是需要通过.value的形式来操作
let {num}=toRefs(reactive(obj))
const btnClick=(()=>{
num.value++
console.log(num);

})
console.log(num);

        return {
num,
btnClick
        }
    }


})



</script>
<style></style>