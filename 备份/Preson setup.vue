<template>
    <div class="person">
        <h2>name:{{name}}</h2>
        <h1>age:{{age}}</h1>
        <button @click="cName">change name</button>
        <button @click="cAge">change age</button>
        <button @click="showTel">tel</button>
    </div>
</template>

<!-- <script lang="ts">
export default {
    name: 'Person',
}
</script> -->
<script setup lang="ts" name="Person123">
let name = '文化'     
let age = 10         
let tel = '12343'
function cName() {
    name = "animals"
}
function cAge() {
    age += 1
}
function showTel() {
    alert(tel)
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
</style>