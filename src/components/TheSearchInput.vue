<script setup>
import { ref } from "vue";
import BaseTooltip from "./BaseTooltip.vue";
import { XMarkIcon, MagnifyingGlassIcon } from "@heroicons/vue/24/outline";

const text = ref("");

const clearInput = () => (text.value = "");
</script>

<template>
  <form class="relative flex w-full items-center">
    <input
      type="text"
      class="w-full rounded-l-full border border-neutral-800 px-4 py-2 outline-0 focus:border-blue-500"
      placeholder="Search"
      v-model="text"
    />
    <button
      type="button"
      class="absolute top-0 right-16 cursor-pointer"
      @click="clearInput"
    >
      <XMarkIcon class="h-10 p-1" />
    </button>
    <BaseTooltip label="Search">
      <button
        type="submit"
        class="cursor-pointer rounded-r-full border border-neutral-800 bg-neutral-800 px-4 py-2 hover:bg-neutral-600"
      >
        <MagnifyingGlassIcon class="h-6" />
      </button>
    </BaseTooltip>
  </form>
</template>

<style lang="scss" scoped></style>
