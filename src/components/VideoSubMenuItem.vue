<script setup>
import BaseIcon from "./BaseIcon.vue";

const props = defineProps({ item: Object });
</script>

<template>
  <a href="#" class="flex items-center gap-4 px-2 py-2 hover:bg-[#555555]">
    <BaseIcon :name="item.icon" />
    <div>{{ icon.label }}</div>
  </a>
</template>
