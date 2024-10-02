<template>
    <div>
    <h1> Ex 4 : </h1>
      <p> tiến độ hoàn thành :  </p>
      <input 
        type="range" 
        v-model="range"  
      />
      <p> Value : {{ range }} %</p>
    </div>
  </template>
  <script setup>
  import { ref } from 'vue';
  const range = ref(' 0');
  </script>
  
  <style > </style>
  