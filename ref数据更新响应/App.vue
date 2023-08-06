<template>
  <div>姓名：{{name}}</div>
  <div>年龄：{{age}}</div>
  <button @click="handleValue">点我改变数据</button>
</template>

<script>
import {ref} from 'vue'

export default {
  setup() {
    let name = ref('路飞')
    let age = ref('18')

   function handleValue() {
      name.value = '索隆'
      age.value = '20'
    }
   
    return {
      name,
      age,
      handleValue
    }
  }
}
</script>

<style>

</style>