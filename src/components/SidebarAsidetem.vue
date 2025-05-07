<script setup>
const props = defineProps({ item: Object });
const { label, icon } = props.item;
</script>

<template>
  <a
    href="#"
    class="flex flex-col gap-1 rounded-lg py-2 text-[10px] outline-none hover:bg-[#292929] focus:bg-[#292929]"
  >
    <component :is="icon" class="h-6"></component>
    <span> {{ label }} </span>
  </a>
</template>
