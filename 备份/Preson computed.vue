<template>
    <div class="person">
        姓：<input type="text" v-model="firstName"><br><br>
        名：<input type="text" v-model="age"><br><br>
        姓名：{{ fullname }}
        <button @click="Changename">change</button>
    </div>
</template>

<script setup lang="ts" name="Person">
    import { reactive,ref, toRefs,toRef, computed } from 'vue';
    let firstName = ref('zhang');
    let age = ref('san');

    let fullname = computed({
        get(){
            return firstName.value.slice(0,1).toUpperCase() +  firstName.value.slice(1) + "-" + age.value;
        },
        set(val){
            const [str1,str2] = val.split('-')
            firstName.value = str1!
            age.value = str2!
            // console.log(x);
        }
    })

    function Changename(){
        fullname.value = "li-si"
        // console.log(fullname.value)
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