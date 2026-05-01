<template>
    <div class="person">
        <h2>一辆{{car.brand}}车，价值{{ car.price }}万</h2>
        <button @click="ChangePrice">Change price</button>
        <button @click="Changecar">品牌修改</button>

        <hr>
        <h2>sss:{{ sum.su }},ddd:{{ sum.brand }}</h2>
        <button @click="Changesum">add</button>
        <button @click="Changetype">type</button>

    </div>
</template>

<script setup lang="ts" name="Person">
import { reactive,ref } from 'vue';
   let car = reactive({brand:'奔驰',price:100})
//    console.log(car)

    let sum = ref({su:100,brand:'sss'})

   function ChangePrice(){
    car.price += 10
    // console.log(car.price)
   }
   function Changesum(){
    sum.value.su += 1
   }
   function Changecar(){
    Object.assign(car,{brand:'奥拓',price:100})
   }
   function Changetype(){
    sum.value = {su:200,brand:'ddd'}
   }
</script>

<style scoped>
.person {
    font-size: 10px;
    background-color: rgb(127, 236, 255);
    box-shadow: 0 0 10px;
    padding: 20px;
}

button {
    margin: 0 5px;
}

li{
    font-size: 20px;
}
</style>