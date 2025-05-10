<script setup>
import SidebarItem from "./SidebarItem.vue";

const moreSection = [
  { label: "YouTube Studio", icon: "youtube-studio" },
  { label: "YouTube Music", icon: "youtube-music-red" },
  { label: "YouTube Kids", icon: "youtube-kids" },
];
</script>

<template>
  <div class="px-10 py-1 text-left font-semibold">More from YouTube</div>
  <ul>
    <li v-for="item in moreSection" :key="item.label" :title="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
