<template>
    <div>
      <h1> Ex 8 : </h1>
      <h3>Đăng nhập tài khoản</h3>
      <form @submit.prevent="handleSubmit">
        <div>
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" required />
        </div>
        <div>
          <label for="password">Mật khẩu</label>
          <input type="password" id="password" v-model="password" required />
        </div>
        <button type="submit">Đăng nhập</button>
        <p v-if="message">{{ message }}</p>
      </form>
    </div>
  </template>

  <script setup>
  import { ref } from 'vue';
  
  const email = ref('');
  const password = ref('');
  const message = ref('');
  
  const handleSubmit = () => {
    if (!email.value || !password.value) {
      message.value = "Email và Mật khẩu không được để trống";
      return;
    }
    const storedUser = JSON.parse(localStorage.getItem("user"));
  
    if (!storedUser) {
      const newUser = {
        email: email.value,
        password: password.value
      };
      localStorage.setItem("user", JSON.stringify(newUser));
      console.log("Tạo thành công");
      message.value = "Tạo tài khoản thành công, đăng nhập thành công!";
    } else {
      if (email.value === storedUser.email && password.value === storedUser.password) {
        message.value = "Đăng nhập thành công";
      } else {
        message.value = "Đăng nhập thất bại";
      }
    }
  };
  </script>
  <style ></style>
  