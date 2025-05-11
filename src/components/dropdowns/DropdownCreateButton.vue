<script setup>
import { PlusIcon } from "@heroicons/vue/24/outline";

const isOpen = defineModel("isOpen");
</script>

<template>
  <button
    class="flex h-10 cursor-pointer items-center justify-center gap-2 rounded-full bg-neutral-800 px-3 hover:bg-neutral-600"
    @click="isOpen = true"
  >
    <PlusIcon class="size-6" />
    <span class="text-sm font-semibold">Create</span>
  </button>
</template>
