<script setup>
import { MagnifyingGlassIcon } from "@heroicons/vue/24/outline";
import TheSearchVoice from "./TheSearchVoice.vue";
import TheSearchInput from "./TheSearchInput.vue";
import TheSearchInputSmall from "./TheSearchInputSmall.vue";
import BaseTooltip from "./BaseTooltip.vue";
import { ref } from "vue";

const isShownInput = ref(false);

const showInput = () => (isShownInput.value = true);
const hideInput = () => (isShownInput.value = false);
</script>

<template>
  <div class="flex-1 items-center sm:flex">
    <div
      class="mx-auto flex w-full max-w-3xl items-center justify-end gap-2 px-2 sm:justify-center"
    >
      <TheSearchInputSmall v-if="isShownInput" @hide-input="hideInput" />
      <TheSearchInput />
      <button
        type="submit"
        class="cursor-pointer rounded-full border-neutral-800 bg-neutral-800 px-4 py-2 hover:bg-neutral-600 sm:hidden"
        @click="showInput"
      >
        <MagnifyingGlassIcon class="h-6" />
      </button>
      <BaseTooltip label="Search with voice">
        <TheSearchVoice />
      </BaseTooltip>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
