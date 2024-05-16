<template>
  <div class="person">
    <h2>一辆车价值：{{car.brand }}车价值{{ car.price }} 万</h2>
    <button @click="changePrice">修改价格</button>
  </div>
  <br>
  <h2>游戏列表：</h2>
  <ul>
    <li v-for="game in games" :key="game.id">{{game.name}}</li>
    <button @click="changeFirstGameName">修改第一个游戏名字</button>
  </ul>
</template>

<script lang="ts">
    export default {
      name: 'Person123',
    }
</script>

<script lang="ts" setup>  //语法糖
   import { reactive } from 'vue';  //修改对象
   // 数据
   let car = reactive({brand: '奔驰', price: 100})   // 被代理变为 Proxy
   let games = reactive([
    {id:"01", name:"LOL"},
    {id:"02", name:"原神"},
    {id:"03", name:"王者农药"}
   ])
   console.log(car)
   function changePrice() {
    car.price += 10
   }
   
   function changeFirstGameName() {
    games[0].name = "魂斗罗"
   }
</script>


<style>
  .person {
    background-color: skyblue;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
  }
  button {
    margin: 0 5px;
  }
  li {
    font-size: 20px;
  }
</style>
