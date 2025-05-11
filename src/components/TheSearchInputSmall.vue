<script setup>
import { defineEmits } from "vue";
import BaseTooltip from "./BaseTooltip.vue";
import { XMarkIcon } from "@heroicons/vue/24/outline";
import { ArrowLeftIcon } from "@heroicons/vue/24/solid";
import SearchButton from "./SearchButton.vue";
const props = defineProps({ query: String, queryModifiers: Object });

const emit = defineEmits({ "update:query": null, hideInput: null });

const updateQuery = (query) => {
  emit("update:query", query);
};
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
      :value="query"
      @input="updateQuery($event.target.value)"
    />
    <button
      type="button"
      class="absolute top-0 right-20 cursor-pointer"
      @click="updateQuery('')"
    >
      <XMarkIcon class="h-10 p-1" />
    </button>
    <BaseTooltip label="Search">
      <SearchButton />
    </BaseTooltip>
  </form>
</template>
