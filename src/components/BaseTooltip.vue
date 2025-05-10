<script setup>
import { ref } from "vue";

const props = defineProps({ label: String, top: Boolean });

const isShown = ref(false);

const showTooltip = () => (isShown.value = true);
const hideTooltip = () => (isShown.value = false);
</script>

<template>
  <div class="relative">
    <div
      @mouseenter="showTooltip"
      @mouseleave="hideTooltip"
      @click="hideTooltip"
    >
      <slot></slot>
    </div>
    <transition
      enter-active-class="transition duration-200"
      enter-from-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="transition duration-200 "
      leave-from-class="opacity-100"
      leave-to-class="opacity-0"
    >
      <div
        :class="`absolute ${top ? '-top-8' : 'top-12'} left-1/2 z-20 -translate-x-1/2 rounded-lg bg-[#444444] px-3 py-1 text-xs font-light whitespace-nowrap text-white`"
        v-if="isShown"
      >
        {{ label }}
      </div>
    </transition>
  </div>
</template>

<style lang="scss" scoped></style>
