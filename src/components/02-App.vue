<template>
  <div>
    <h2 ref='op'>wspl</h2>
  </div>
</template>

<script  lang='ts'>
import {defineComponent,ref,onMounted,nextTick,reactive} from 'vue'
export default defineComponent({
  setup(){
    let op=ref() //绑定ref属性  其值为op的标签
    console.log(op.value); //undefined 获取的时机不对
    onMounted(()=>{
      console.log("onMounted",op.value);
      
    } )
let obj={
  num:20
}
//ref 用来实现基础数据类型的 
// reactive用来实现复杂数据类型的响应式
    let objRef=reactive(obj)
console.log(objRef);
    nextTick(()=>{
      console.log("nexTick",op.value);
      
    })
    return {
      op
    }
    
  }
})
</script>

<style scoped>

</style>
