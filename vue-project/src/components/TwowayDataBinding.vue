<template>
  <form @submit.prevent="handleSubmit">
    <h2>UserName: {{ userInfo.userName }}</h2>
    <h2>DateOfBirth: {{ userInfo.dateOfBirth }}</h2>
    <h2>Gender: {{ userInfo.gender }}</h2>
    <h2>Hobbies: {{ userInfo.hobbies }}</h2>

    <h3>Thêm mới người dùng</h3>
    <div>
      Họ và tên:
      <input v-model="userInfo.userName" type="text" placeholder="Nhập tên" />
    </div>
    <div>Ngày sinh: <input v-model="userInfo.dateOfBirth" type="date" /></div>
    <div>Giới tính:</div>
    <div>
      Nam
      <input name="gender" v-model="userInfo.gender" type="radio" value="0" />
      Nữ
      <input name="gender" v-model="userInfo.gender" type="radio" value="1" />
      Khác
      <input name="gender" v-model="userInfo.gender" type="radio" value="2" />
    </div>
    <div>Sở thích</div>
    <div>
      Chơi game
      <input value="code" v-model="userInfo.hobbies" type="checkbox" /> Code
      <input value="swim" type="checkbox" v-model="userInfo.hobbies" /> Bơi lội
      <input value="volleyball" type="checkbox" v-model="userInfo.hobbies" />
      Bóng chuyền
      <input value="soccer" type="checkbox" v-model="userInfo.hobbies" /> Bóng
      đá
    </div>
    <button>Thêm</button>
  </form>
</template>
<script setup>
import { reactive } from "vue";

const userInfo = reactive({
  userName: "",
  dateOfBirth: "",
  gender: "0",
  hobbies: [],
});

const handleSubmit = (e) => {
  // Ngăn chặn sự kiện load lại trang
  //   e.preventDefault();

  console.log("Submited: ", userInfo);
};
</script>

<style></style>