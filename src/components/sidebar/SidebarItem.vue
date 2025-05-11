<script setup>
import BaseIcon from "../BaseIcon.vue";

const props = defineProps({ item: Object });
</script>

<template>
  <a
    href="#"
    class="mx-4 mr-auto flex items-center gap-6 rounded-xl px-4 py-2 text-sm outline-none hover:bg-[#232323]"
  >
    <BaseIcon :name="item.icon" />
    <span>{{ item.label }}</span>
  </a>
</template>
