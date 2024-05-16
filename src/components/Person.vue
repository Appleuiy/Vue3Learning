<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <h2>地址：{{address }}</h2>
    <button @click="changeName">名字变一变</button>
    <button @click="changeAge">年龄+1</button>
    <button @click="showTel">点我拿电话</button>
  </div>
</template>

<script lang="ts">
    export default {
      name: 'Person123',
    }
</script>

<script lang="ts" setup>  //语法糖
    import {ref} from 'vue'  //ref创建响应式数据
    let age = ref(22)
    let name = ref("张飘")  // 加上ref， 修改时候要对value更改   
    let tel = "15085462605" 
    let address = "北京市海淀区知春路大运村学生公寓"
    function changeAge() {
      age.value += 1
    }

    function changeName() {
      name.value = "夏思嘉必定考好"  
      console.log(name) 
    }

    function showTel() {
      alert(age)
    }
</script>


<style>
  .person {
    background-color: skyblue;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
  }
</style>
