<template lang="">
  <div>
    222222
    {{num}}
    <button @click="bdClick">点击按钮</button>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref ,onMounted,nextTick} from 'vue'

export default defineComponent({
  setup() {
    let num = ref(20) //这个num是Vue 内部封装的一个响应式的数据
    console.log('什么时候执行了setup');
    console.log(num.value);

    const bdClick = () => {
      num.value++
    }
onMounted(()=>{
  console.log("onMunted",num.value);
  
})
    nextTick()
    return {
      num,
      bdClick
    }

  },

})
</script>
<style lang="">
  
</style>