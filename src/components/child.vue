<template>
  <!-- 子组件   -->
  <p>{{num}}</p>
  <button @click="hdClick">子组件传参给父组件</button>
</template>

<script lang='ts' setup>
import { defineProps,defineEmits  } from 'vue' 
        defineProps({
            num:{
                type:Number,
                defalut:30
            }
        })

      // 子传父的时候需要先定义好emit好这个方法
        const emit =defineEmits<{
          (event:'fn',val:number):void
        }>()

        
        const hdClick=()=>{
          // 以前通过$emit("自定义事件",参数)
            emit('fn',10)
        }
</script>
 
<style lang= "less" scoped>
    
</style>