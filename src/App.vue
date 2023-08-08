<template>
   姓： <input type="text" name="" id="" v-model="person.firstName"> <br>
   名： <input type="text" name="" id="" v-model="person.lastName">
   <br>
   <hr>
   <span>全名：{{person.fullName}}</span>
   <br>
   <hr>
   修改：<input type="text" v-model="person.fullName">
</template>

<script>
import {ref,reactive,computed} from 'vue'

export default {
  setup() {
   let person = reactive({ 
    firstName:'路',
    lastName:'飞'
   })


   //直接person.fullName是可以追加属性的
   //简写 （没有修改操作，只能读数据）
   person.fullName = computed(()=>{
    return person.firstName + '-' + person.lastName
   }) 


  // //完整写法
  //   person.fullName = computed({
  //     get() {
  //       return person.firstName + '-' + person.lastName
  //     },
  //     set(value) {
  //       const newArr = value.split('-')
  //       person.firstName = newArr[0]
  //       person.lastName = newArr[1]
  //     }
  //   })

    return {
       person
    }
  }
}
</script>

<style>

</style>