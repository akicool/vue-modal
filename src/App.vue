<script setup>
import { ref } from "vue";
import Button from "./components/Button.vue";
import Modal from "./components/Modal.vue";

const modalOpen = ref(false);

const openModal = () => {
  modalOpen.value = true;
};

const closeModal = () => {
  modalOpen.value = false;
}; 
</script>

<template>
  <div class="relative bg-[#1c1c1c] text-white w-full h-screen grid place-items-center">
    <Button @click="openModal" />
    <Modal :isOpen="modalOpen" @buttonCloseModal="closeModal" />
  </div>
</template>

<style scoped></style>
