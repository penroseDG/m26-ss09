<template> 
<div>
    <h1> Ex 2 : </h1>
    <p> Color  : </p>
    <input type="color" v-model="color">
    <p> color code : {{ color }}</p>
</div>
</template>

<script setup>
import {ref} from 'vue';
 const color = ref('#fff') ;
</script>
<style></style>