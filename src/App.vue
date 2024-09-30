<template>
  <div>
    <h1>Home Page</h1>
    <p>____________________________________________</p>
    <ParentComponent />

    <!-- <BaseButton /> -->
    <!-- <BaseButton title="Add product" /> -->

    <!-- Nội dung này sẽ chính là slot sau này dùng -->
    <!-- <SlotComponent>
      <a href="">Facebook</a>
    </SlotComponent> -->

    <BaseButton @onClick="handleClickParent">
      <!-- <div>Click me</div> -->
    </BaseButton>
  </div>
</template>

<script setup>
import BaseButton from "./components/BaseButton.vue";
import ParentComponent from "./components/ParentComponent.vue";
import SlotComponent from "./components/SlotComponent.vue";

const handleClick = () => {
  console.log("Clicked");
};

const handleClickParent = (data) => {
  console.log("Dữ liệu truyền từ con: ", data);
};
</script>

<style></style>
