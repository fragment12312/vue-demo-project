<template>
    <div class="person">
        <h2>name:{{name}}</h2>
        <h1>age:{{age}}</h1>
        <button @click="cName">change name</button>
        <button @click="cAge">change age</button>
        <button @click="showTel">tel</button>
        <div>ddd:{{ sss }}</div>
        <h2>ddd:{{ c }}</h2>
    </div>
</template>

<script>
export default {
    name: 'Person',
    data(){
        return {
            sss:100,
            c:this.name
        }
    },
    setup(){//vue3弱化了this
        //data
        let name = '文化'     //不是响应式
        let age = 10         //不是响应式
        let tel = '12343'
    //methods
        function cName() {
            name = "animals"
        }
        function cAge() {
            age += 1         //name,age都改变了，只是数据并非响应式
        }
        function showTel() {
            alert(tel)
        }
        return {name,age,cName,cAge,showTel}//交出数据
        // return ()=> 'sss' //有这个写法
    }
}
</script>

<style>
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