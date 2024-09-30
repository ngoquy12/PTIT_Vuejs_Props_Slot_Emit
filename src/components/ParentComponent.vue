<template>
  <div>
    <h1>Parent component</h1>
    <h3>UserName of ParentComponent: {{ userName }}</h3>
    <p>____________________________________________</p>

    <!-- Sử dụng Component con -->
    <!-- Bước 2: Trong component cha, gọi props được khai báo bên con và truyền giá trị cho nó -->
    <ChildrenComponent
      :userInfoProps="userInfo"
      :userNameProps="userName"
      :ageProps="age"
    />
  </div>
</template>

<script setup>
import ChildrenComponent from "./ChildrenComponent.vue";

const userName = "Nguyễn Văn A";

// Tạo biến tuổi, truyền từ ParentComponent xuống ChildrenComponent
const age = 20;

const userInfo = {
  id: 1,
  name: "Nguyễn Văn B",
  age: 21,
};
</script>

<style></style>
