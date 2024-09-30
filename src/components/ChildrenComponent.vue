<template>
  <div>
    <h1>Children component</h1>
    <!-- Bước 3: Lấy giá trị từ props và render dữ liệu -->
    <h3>UserName of ChildrenComponent: {{ userNameProps }}</h3>
    <h3>Age of ChildrenComponent: {{ ageProps }}</h3>
  </div>
</template>

<script setup>
// Bước 1: Định nghĩa props bên trong component con
const { userNameProps, ageProps, userInfoProps } = defineProps([
  "userNameProps",
  "ageProps",
  "userInfoProps",
]);

console.log("userInfoProps: ", userInfoProps);
</script>

<style></style>
