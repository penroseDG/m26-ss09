<template>
      <div>
      <h1> Ex 1 : </h1>
        <p>Email : </p>
        <input  type="email" v-model="email" placeholder="Nhập email của bạn"/>
        <p> Value : {{ email }}</p>
      </div>
    </template>
    <script setup>
    import { ref } from 'vue';
    const email = ref(' ');
    </script>
    
    <style >
    </style>
    