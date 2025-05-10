<script setup>
import { icons } from "@/icons";
const path = defineProps({ name: String });
</script>

<template>
  <div>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      fill="currentColor"
      height="24"
      viewBox="0 0 24 24"
      width="24"
      focusable="false"
      aria-hidden="true"
      v-html="icons[name]"
    ></svg>
  </div>
</template>
