<script setup>
import { ref } from "vue";

const props = defineProps({ label: String, top: Boolean });

const isShown = ref(false);
const classes = [
  "absolute left-1/2 z-20 -translate-x-1/2 rounded-lg bg-[#444444] px-3 py-1 text-xs font-light whitespace-nowrap text-white",
  { "-top-8": props.top },
];

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
      <div :class="classes" v-if="isShown">
        {{ label }}
      </div>
    </transition>
  </div>
</template>


