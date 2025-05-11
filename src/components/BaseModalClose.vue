<script setup>
import { XMarkIcon } from "@heroicons/vue/24/outline";

const emit = defineEmits({ closeModal: null });
</script>

<template>
  <div>
    <button
      class="absolute top-4 right-4 cursor-pointer rounded-full hover:bg-neutral-700"
      @click="emit('closeModal')"
    >
      <XMarkIcon class="h-8" />
    </button>
  </div>
</template>


