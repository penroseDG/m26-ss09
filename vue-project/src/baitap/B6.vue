<template>
    <div>
      <h1> Ex 6 : </h1>
      <p>Sở thích: {{ hobbies }}</p>
      <div>
        <label>
          <input value="Đá bóng" v-model="hobbies" type="checkbox" />
          Đá bóng
        </label>
        <label>
          <input value="Bóng chuyền" v-model="hobbies" type="checkbox" />
          Bóng chuyền
        </label>
        <label>
          <input value="Code" v-model="hobbies" type="checkbox" />
          Code
        </label>
        <label>
          <input value="Bơi lội" v-model="hobbies" type="checkbox" />
          Bơi lội
        </label>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  const hobbies = ref([]);
  </script>

  <style></style>