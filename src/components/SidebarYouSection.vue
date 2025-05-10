<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/solid";
import SidebarItem from "./SidebarItem.vue";

const youSection = [
  { label: "History", icon: "youtube-history" },
  { label: "Playlists", icon: "youtube-playlist" },
  { label: "Your videos", icon: "youtube-videos" },
  { label: "Watch later", icon: "youtube-watch-later" },
  { label: "Liked videos", icon: "youtube-like" },
  { label: "Downloads", icon: "youtube-downloads" },
];
</script>

<template>
  <ul>
    <li
      class="mx-4 flex items-center justify-between gap-6 rounded-xl px-4 py-2 font-semibold outline-none hover:bg-[#232323]"
    >
      <span>You</span><ChevronRightIcon class="h-6" />
    </li>
    <li v-for="item in youSection" :key="item.label" :title="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
