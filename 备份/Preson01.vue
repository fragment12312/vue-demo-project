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
<script setup lang="ts" name="Person">
    import {ref} from 'vue'

let name = ref('文化')     
let age = ref(10)       
let tel = '12343'
// console.log(1,name);
// console.log(2,tel);
function cName() {
    name.value = "animals"
}
function cAge() {
    age.value += 1
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