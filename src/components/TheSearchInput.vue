<script setup>
import BaseTooltip from "./BaseTooltip.vue";
import { XMarkIcon, MagnifyingGlassIcon } from "@heroicons/vue/24/outline";
import SearchButton from "./SearchButton.vue";

const props = defineProps({ query: String, queryModifiers: Object });
const emit = defineEmits({ "update:query": null });

const updateQuery = (query) => {
  emit("update:query", query);
};
</script>

<template>
  <div class="relative hidden w-full items-center sm:flex">
    <input
      type="text"
      class="w-full rounded-l-full border border-neutral-800 px-4 py-2 outline-0 focus:border-blue-500"
      placeholder="Search"
      :value="query"
      @input="updateQuery($event.target.value)"
    />
    <div></div>
    <button
      type="button"
      class="absolute top-0 right-16 hidden cursor-pointer sm:block"
      @click="updateQuery('')"
    >
      <XMarkIcon v-if="query" class="h-10 p-1" />
    </button>
    <BaseTooltip label="Search">
      <SearchButton />
    </BaseTooltip>
  </div>
</template>

<style lang="scss" scoped></style>
