<script setup>
const footer = [
  "Terms",
  "Privacy $ Safety",
  "How Youtube works",
  "Test new features",
];
</script>

<template>
  <ul
    class="flex flex-wrap gap-1 px-8 pt-4 text-xs font-semibold text-[#aaaaaa]"
  >
    <li v-for="item in footer" :key="item">
      <a href="#" class="p-1 outline-none focus:bg-[#232323]">{{ item }}</a>
    </li>
  </ul>
</template>
