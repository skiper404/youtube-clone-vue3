<script setup>
import { defineEmits, ref } from "vue";
import BaseTooltip from "./BaseTooltip.vue";
import { XMarkIcon, MagnifyingGlassIcon } from "@heroicons/vue/24/outline";
import { ArrowLeftIcon } from "@heroicons/vue/24/solid";

const emit = defineEmits({
  hideInput: null,
});

const text = ref("");
const clearInput = () => (text.value = "");
</script>

<template>
  <form class="fixed top-2 right-0 left-0 z-20 flex items-center bg-black px-2">
    <BaseTooltip label="Back">
      <ArrowLeftIcon class="h-8 cursor-pointer" @click="emit('hideInput')" />
    </BaseTooltip>
    <input
      type="text"
      class="ml-2 w-full rounded-l-full border border-neutral-800 px-4 py-2 outline-0"
      placeholder="Search"
      v-model="text"
    />
    <button
      type="button"
      class="absolute top-0 right-20 cursor-pointer"
      @click="clearInput"
    >
      <XMarkIcon class="h-10 p-1" />
    </button>
    <BaseTooltip label="Search">
      <button
        type="submit"
        class="cursor-pointer rounded-r-full border-neutral-800 bg-neutral-800 px-4 py-2 hover:bg-neutral-600"
      >
        <MagnifyingGlassIcon class="h-6" />
      </button>
    </BaseTooltip>
  </form>
</template>
