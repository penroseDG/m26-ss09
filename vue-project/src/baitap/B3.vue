<template>
    <div>
        <h1> Ex 3 : </h1>
        <p> Date of Birth : {{  dateOfBirth }}</p>
        <input type= "date" placeholder=" nhập ngày sinh của bạn zô đây đi babe " v-model="dateOfBirth" >
    </div>
</template>
<script setup >
 import {ref} from 'vue' ; 
 const dateOfBirth = ref("xx/yy/xxyy")

</script>

<style></style>