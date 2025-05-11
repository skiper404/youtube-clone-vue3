<script setup>
import { onMounted, onBeforeUnmount } from "vue";
import BaseModalClose from "./BaseModalClose.vue";

const emit = defineEmits({ closeModal: null });

const handleKeyDown = (event) => {
  if (event.key === "Escape") {
    emit("closeModal");
  }
};

onMounted(() => {
  window.addEventListener("keydown", handleKeyDown);
});

onBeforeUnmount(() => {
  window.removeEventListener("keydown", handleKeyDown);
});
</script>
<template>
  <div
    class="fixed inset-0 z-20 cursor-pointer bg-black/50"
    @click.self="emit('closeModal')"
  >
    <div
      class="relative mx-auto mt-16 h-[400px] rounded-xl bg-[#242424] p-4 sm:w-[500px]"
    >
      <BaseModalClose @close-modal="emit('closeModal')" />
      <slot></slot>
    </div>
  </div>
</template>


