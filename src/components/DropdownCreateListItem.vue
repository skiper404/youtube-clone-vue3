<script setup>
const props = defineProps(["item"]);
</script>

<template>
  <a href="#" class="flex items-center gap-4 px-6 outline-none">
    <component :is="item.icon" class="h-6" />
    <hr />
    <span> {{ item.label }} </span>
  </a>
</template>
