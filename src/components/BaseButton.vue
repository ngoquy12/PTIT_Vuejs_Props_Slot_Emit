<template>
  <!-- Bước 2: Phát sự kiện thông qua emit -->
  <button @click="handleClick">
    <!-- <slot></slot> -->
    click me
  </button>
</template>

<script setup>
const props = defineProps({
  title: {
    default: "Click me 1",
    type: String,
    required: true,
  },
});

// Bước 1:KHởi tạo ra các emit
const emit = defineEmits(["onClick"]);
console.log("Props: ", props);

const handleClick = () => {
  emit("onClick", "Xin chào các bạn PTIT 2023");
};
</script>

<style></style>
