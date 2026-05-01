<template>
    <div class="person">
        <h2>name:{{ person.name }}</h2>
        <h2>age:{{ person.age }}</h2>
        <button @click="CN">ChangeName</button>
        <button @click="CA">ChangeAge</button>
    </div>
</template>

<script setup lang="ts" name="Person">
    import { reactive,ref, toRefs } from 'vue';
    let person = reactive({
        name:"sss",
        age:18
    })

    let {name,age} = toRefs(person)

    function CN(){
        name.value += '~'
    }
    function CA(){
        age.value += 1
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