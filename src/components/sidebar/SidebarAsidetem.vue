<script setup>
import BaseIcon from "../BaseIcon.vue";

const props = defineProps({ item: Object });
</script>

<template>
  <a
    href="#"
    class="flex flex-col items-center gap-1 rounded-lg py-2 text-[10px] outline-none hover:bg-[#292929] focus:bg-[#292929]"
  >
    <BaseIcon :name="item.icon" />
    <span> {{ item.label }} </span>
  </a>
</template>
