<template>
  <div>姓名：{{name}}</div>
  <div>年龄：{{age}}</div>
  <div @click="sayHellow">打招呼</div>
</template>

<script>
export default {
  setup() {
    let name = '路飞'
    let age = '18'

    function sayHellow () {
      alert(`您好，我叫${name},今年${age}岁`)
    }

    return {
      name,
      age,
      sayHellow
    }
  }
}
</script>

<style>

</style>