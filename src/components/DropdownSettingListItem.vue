<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/outline";

const props = defineProps({ item: Object });
const { label, icon, submenu } = props.item;
</script>

<template>
  <a
    href="#"
    class="flex items-center gap-4 px-4 py-2 outline-none hover:bg-[#555555]"
  >
    <component :is="icon" class="h-6"></component>
    <span>{{ label }}</span>
    <ChevronRightIcon v-if="submenu" class="ml-auto h-6" />
  </a>
</template>

<style lang="scss" scoped></style>
