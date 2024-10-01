<template>
  <h1>ListUser</h1>
  <h2>Count: {{ count }}</h2>

  <button @click="handleShowForm">Show form</button>

  <p>-----------------------------------</p>

  <!-- Hiển thị Form -->
  <FormComponent
    @onCount="handleCount"
    v-if="isShow"
    @onClose="handleCloseForm"
  />
</template>

<script setup>
import { ref } from "vue";
import FormComponent from "./FormComponent.vue";

const isShow = ref(false);
const count = ref(0);

// Hàm mở form
const handleShowForm = () => {
  // Cập nhật lại giá trị cho biến isShow
  isShow.value = true;
};

const handleCloseForm = () => {
  isShow.value = false;
};

const handleCount = () => {
  count.value++;
};
</script>

<style></style>
