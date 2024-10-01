<template>
  <!-- Bước 2: Bắt sự kiện trong component con -->
  <button @click="handleClose">Close</button>
  <button @click="handleCount">Count</button>
  <h1>Form Component</h1>
</template>

<script setup>
// Bước 1: Định nghĩa emit trong component con
const emit = defineEmits(["onClose", "onCount"]);

const handleClose = () => {
  // Bắn một emit
  emit("onClose");
};

const handleCount = () => {
  emit("onCount");
};
</script>

<style></style>
