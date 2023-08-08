<template>
  <div>姓名：{{name}}</div>
  <div>年龄：{{age}}</div>
  <div>技能：{{hzwObj.jineng}}</div>
  <div>职位：{{hzwObj.zhiwei}}</div>
  <button @click="handleValue">点我改变数据</button>
</template>

<script>
import {ref,reactive} from 'vue'

export default {
  setup() {
    let name = ref('路飞')
    let age = ref('18')


    // let hzwObj = ref({
    //       jineng:'四档·蛇人',
    //       zhiwei:'船长'
    //     })

    let hzwObj = reactive({
      jineng:'四档·蛇人',
      zhiwei:'船长'
    })

    


   function handleValue() {
      name.value = '索隆'
      age.value = '20'

      //ref使用方法
     /*  hzwObj.value.jineng = '五档·尼卡形态'
      hzwObj.value.zhiwei = '大船长' */

      //reactive使用方式
      hzwObj.jineng = '五档·尼卡形态'
      hzwObj.zhiwei = '大船长'
    }
   
    return {
      name,
      age,
      hzwObj,
      handleValue,
    }
  }
}
</script>

<style>

</style>