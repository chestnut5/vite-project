<template>
<input type="checkbox" v-model="checkAll">全选或反选
<ul>
    <li v-for="item,index in list" :key="index">
        <input type="checkbox" v-model="checkList[index]">{{item}}
    </li>
</ul>



</template>

<script lang='ts' setup>
import { toRefs, ref,reactive,computed } from 'vue' 
    
     let data=reactive<DataType>({
        list:[10,20,30,40]
        ,
        checkList:[]
        // 一个数据，如果在视图上有使用到，就需要写到toRefs解构里面去 如果只是在js环境临时用
        // 视图不需要用 那么就不需要参与解构
     }) 

     data.checkList=data.list.map(()=>false)
     let {list,checkList} =toRefs(data) 


let checkAll=computed({
    get:(()=>{
        // checkList包含一个false就返回false
        
      return !data.checkList.includes(false)
    }),
    set:((newVal:boolean)=>{
       data.checkList=data.checkList.map(()=>newVal)
    })
})
</script>
 
<style lang= "less" scoped>
    
</style>