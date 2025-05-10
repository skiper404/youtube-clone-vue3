<script setup>
import { computed } from "vue";
import BaseIcon from "./BaseIcon.vue";
const props = defineProps(["category", "isActive"]);

const classes = computed(() => [
  "rounded-lg bg-[#232323] px-2 py-1 hover:bg-[#333333]",
  { "bg-[#eeeeee] text-black": props.isActive === props.category },
]);
</script>

<template>
  <BaseIcon name="youtube" class="h-10" />
  <a href="#" :class="classes">{{ category }}</a>
</template>

<style lang="scss" scoped></style>
