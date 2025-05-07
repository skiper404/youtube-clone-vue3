<script setup>
const props = defineProps({ item: Object });
const { label, icon } = props.item;
</script>

<template>
  <a
    href="#"
    class="mx-4 flex items-center gap-6 rounded-xl px-4 py-2 text-sm outline-none hover:bg-[#232323]"
  >
    <component :is="icon" class="h-6"></component>
    <span>{{ label }}</span>
  </a>
</template>
