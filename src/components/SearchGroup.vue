<script setup>
import { MagnifyingGlassIcon } from "@heroicons/vue/24/outline";
import TheSearchVoice from "./TheSearchVoice.vue";
import TheSearchInput from "./TheSearchInput.vue";
import TheSearchInputSmall from "./TheSearchInputSmall.vue";
import BaseTooltip from "./BaseTooltip.vue";
import TheSearchResults from "./TheSearchResults.vue";
import { computed, onMounted, onUnmounted, ref } from "vue";

const isShownInput = ref(false);
const query = ref("");

let keywords = [
  "new york",
  "new york city",
  "new york weather",
  "new york time",
  "new york map",
  "new york subway",
  "new york attractions",
  "new york hotels",
  "new york taxi",
];

const filteredResults = computed(() =>
  keywords.filter((keyword) =>
    keyword.toLowerCase().includes(trimmedQuery.value),
  ),
);

const closeByEsc = (event) => {
  if (event.key === "Escape") {
    isSearchFocused.value = false;
  }
};

onMounted(() => window.addEventListener("keydown", closeByEsc));
onUnmounted(() => window.removeEventListener("keydown", closeByEsc));

const trimmedQuery = computed(() => query.value.replace(/\s+/g, " ").trim());

const isSearchFocused = ref(true);
const isSearchResultsShown = computed(
  () => isSearchFocused.value && query.value.length,
);

const showInput = () => (isShownInput.value = true);
const hideInput = () => (isShownInput.value = false);

const pasteKeywordToInput = (keyword) => (query.value = keyword);
</script>

<template>
  <div class="flex-1 items-center sm:flex">
    <div
      class="mx-auto flex w-full max-w-3xl items-center justify-end gap-2 px-2 sm:justify-center"
    >
      <TheSearchInputSmall
        v-if="isShownInput"
        @hide-input="hideInput"
        v-model:query="query"
      />

      <div class="relative w-full" ref="wrapper">
        <TheSearchInput
          class="w-full"
          v-model:query="query"
          @focus="isSearchFocused = true"
          @blur="isSearchFocused = false"
        />
        <TheSearchResults
          :result="filteredResults"
          v-if="isSearchResultsShown"
          @set-keyword-to-input="pasteKeywordToInput"
        />
      </div>
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
