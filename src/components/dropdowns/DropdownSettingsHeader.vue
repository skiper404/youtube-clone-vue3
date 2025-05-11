<script setup>
import { ArrowLeftIcon } from "@heroicons/vue/24/outline";
const props = defineProps({ label: String, desctiption: String });
const emit = defineEmits({ back: null });
</script>

<template>
  <div class="flex items-center gap-4 border-b border-[#555555] p-3">
    <button
      class="focus-outline: none cursor-pointer"
      @click.stop="emit('back')"
    >
      <ArrowLeftIcon class="h-6" />
    </button>
    <span>{{ label }}</span>
  </div>
  <div class="my-2 py-2 pl-4 text-start text-xs font-light" v-if="desctiption">
    {{ desctiption }}
  </div>
</template>
