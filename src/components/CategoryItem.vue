<script setup>
import { computed } from "vue";

const props = defineProps(["category", "isActive"]);

const classes = computed(() => [
  "rounded-lg bg-[#232323] px-2 py-1 hover:bg-[#333333]",
  {
    "bg-[#eeeeee] text-black hover:bg-[#ccccc]":
      props.isActive === props.category,
  },
]);
</script>

<template>
  <a href="#" :class="classes">{{ category }}</a>
</template>


