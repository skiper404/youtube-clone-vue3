<script setup>
import { MagnifyingGlassIcon } from "@heroicons/vue/24/outline";

const props = defineProps({ result: Array });
const emit = defineEmits({ setKeywordToInput: String });
</script>

<template>
  <div
    class="absolute top-full left-0 hidden w-full rounded-2xl bg-[#1e1e1e] py-4 sm:block"
  >
    <ul>
      <li
        v-for="keyword in result"
        class="flex items-center gap-4 px-6 py-2 hover:bg-[#555555]"
        @click="$emit('set-keyword-to-input', keyword)"
      >
        <MagnifyingGlassIcon class="h-6" />
        <span class="truncate">
          {{ keyword }}
        </span>
      </li>
    </ul>
  </div>
</template>
