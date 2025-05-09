<script setup>
import { ref } from "vue";

const props = defineProps({ label: String });

const isShowTooltip = ref(false);

const showTooltip = () => (isShowTooltip.value = true);
const hideTooltip = () => (isShowTooltip.value = false);
</script>

<template>
  <div class="relative">
    <div @mouseenter="showTooltip" @mouseleave="hideTooltip">
      <slot></slot>
    </div>
    <div
      class="absolute top-12 left-1/2 z-20 -translate-x-1/2 rounded-lg bg-[#444444] px-3 py-1 text-xs font-light whitespace-nowrap"
      v-if="isShowTooltip"
    >
      {{ label }}
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
