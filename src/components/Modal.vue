<script setup>
import { defineProps, defineEmits } from "vue";

const props = defineProps(["isOpen"]);
const emits = defineEmits(["buttonCloseModal"]);

const buttonCloseModal = () => {
  emits("buttonCloseModal");
};
</script>

<template>
  <div
    class="absolute flex flex-col items-center gap-6 px-10 py-6 bg-slate-600 rounded-xl left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 transition duration-300"
    :class="isOpen ? 'opacity-1 z-10' : 'opacity-0'"
  >
    <label class="swap swap-flip text-9xl">
      <input type="checkbox" />

      <div class="swap-off">😎</div>
      <div class="swap-on">🤓</div>
    </label>
    <button @click="buttonCloseModal" class="btn btn-accent max-w-[5rem]">
      close
    </button>
  </div>
</template>

<style scoped></style>
