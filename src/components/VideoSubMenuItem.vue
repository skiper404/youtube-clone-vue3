<script setup>
import BaseIcon from "./BaseIcon.vue";

const props = defineProps({ item: Object });
const { label, icon } = props.item;
</script>

<template>
  <a href="#" class="flex items-center gap-4 px-2 py-2 hover:bg-[#555555]">
    <BaseIcon :name="icon" />
    <div>{{ label }}</div>
  </a>
</template>

<style lang="scss" scoped></style>
