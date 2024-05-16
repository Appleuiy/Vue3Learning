<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
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
    let age = "22"
    let name = "张飘"
    let tel = "15085462605" 

    function changeAge() {
      age += 1
    }

    function changeName() {
      name = "夏思嘉必定考好"  
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
