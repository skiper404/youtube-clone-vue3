<script setup>
import { BellIcon } from "@heroicons/vue/24/outline";

const isOpen = defineModel("isOpen");
</script>

<template>
  <button
    class="cursor-pointer rounded-full p-1 hover:bg-neutral-600"
    @click="isOpen = true"
  >
    <BellIcon class="size-7" />
  </button>
</template>
