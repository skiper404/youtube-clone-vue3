<script setup>
import { ref } from "vue";
import CategoryItem from "./CategoryItem.vue";

const categories = [
  "All",
  "Poscasts",
  "Music",
  "Mixes",
  "Apple",
  "Tesla",
  "Blogs",
  "Satire",
  "Live",
  "Gadges",
  "Computers",
  "Rapping",
  "Electronic",
  "Watched",
  "New to you",
];

const isActive = ref("All");
</script>

<template>
  <section
    class="fixed top-14 right-0 left-0 z-10 bg-[#121212]/95 p-2 text-[16px] md:left-36 xl:left-66"
  >
    <div
      class="pointer-events-none absolute inset-0 -z-10 backdrop-blur-xs"
    ></div>
    <ul
      class="scrollbar-hide flex items-center gap-2 overflow-auto px-2 py-1 whitespace-nowrap"
    >
      <li v-for="category in categories" :key="category">
        <CategoryItem :category="category" :is-active="isActive" />
      </li>
    </ul>
  </section>
</template>
