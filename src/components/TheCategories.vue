<script setup>
import { ref } from "vue";
import CategoryList from "./CategoryList.vue";
import BlurLayout from "./BlurLayout.vue";

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

const setActive = (category) => (isActive.value = category);
</script>

<template>
  <section
    class="fixed top-14 right-0 left-0 z-10 bg-[#121212]/95 p-1 text-[16px] md:left-36 xl:left-66"
  >
    <BlurLayout />
    <CategoryList
      :categories="categories"
      :is-active="isActive"
      @set-active="setActive"
    />
  </section>
</template>
