<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/outline";
import BaseIcon from "./BaseIcon.vue";

const props = defineProps({ item: Object });
const { label, icon, submenu } = props.item;

console.log(icon);
</script>

<template>
  <a
    href="#"
    class="flex items-center gap-4 px-4 py-2 outline-none hover:bg-[#555555]"
  >
    <BaseIcon class="h-6" :name="icon" />
    <span>{{ label }}</span>
    <ChevronRightIcon v-if="submenu" class="ml-auto h-6" />
  </a>
</template>

<style lang="scss" scoped></style>
