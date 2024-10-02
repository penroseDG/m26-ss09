<template>
    <div>
      <h1>Ex 5:</h1>
      <p>Giới tính: {{ userInfo.gender }}</p>
      <div>
        <label>
          <input name="gender" v-model="userInfo.gender" type="radio" value="Nam" />
          Nam
        </label>
        <label>
          <input name="gender" v-model="userInfo.gender" type="radio" value="Nữ" />
          Nữ
        </label>
        <label>
          <input name="gender" v-model="userInfo.gender" type="radio" value="Gay" />
          Khác
        </label>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  const userInfo = ref({gender: '' });
  </script>
  
  <style></style>