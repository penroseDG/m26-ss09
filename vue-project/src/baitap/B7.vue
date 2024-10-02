<template>
    <div>
      <h1> Ex 7 : </h1> 
      <p>------------------------</p>
      <h3>Thêm mới sản phẩm </h3>
      <p>------------------------</p>
      <form @submit.prevent="addProduct">
        <div>
          <label for="productId">Mã sản phẩm</label>
          <input type="text" id="productId" v-model="product.productId" required />
        </div>
        <div>
          <label for="productName">Tên sản phẩm</label>
          <input type="text" id="productName" v-model="product.productName" required />
        </div>
        <div>
          <label for="price">Giá</label>
          <input type="number" id="price" v-model="product.price" required />
        </div>
        <div>
          <label for="quantity">Số lượng</label>
          <input type="number" id="quantity" v-model="product.quantity" required />
        </div>
        <button type="submit">Thêm mới</button>
      </form>
    </div>
  </template>
  
  <script setup>
  import { reactive } from 'vue';
  const product = reactive({
    productId: '',
    productName: '',
    price: 0,
    quantity: 0
  });
  
  const addProduct = () => {
    console.log(product);
  };
  </script>
  
  <style scoped>
  form {
    display: flex;
    flex-direction: column;
    width: 300px;
  }
  
  div {
    margin-bottom: 10px;
  }
  
  button {
    background-color: blue;
    color: white;
    padding: 10px;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: darkblue;
  }
  
  input {
    padding: 8px;
    width: 100%;
    box-sizing: border-box;
  }
  </style>
  