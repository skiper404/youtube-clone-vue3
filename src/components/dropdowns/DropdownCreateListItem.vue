<script setup>
import BaseIcon from "../BaseIcon.vue";

const props = defineProps(["item"]);
</script>

<template>
  <a href="#" class="flex items-center gap-4 px-6 outline-none">
    <BaseIcon :name="item.icon" />
    <span> {{ item.label }} </span>
  </a>
</template>
