<script setup>
const props = defineProps({ item: Object });
const { label, icon } = props.item;
</script>

<template>
  <a href="#" class="flex items-center gap-4 px-2 py-2 hover:bg-[#555555]">
    <component :is="icon" class="h-6"></component>
    <div>{{ label }}</div>
  </a>
</template>

<style lang="scss" scoped></style>
