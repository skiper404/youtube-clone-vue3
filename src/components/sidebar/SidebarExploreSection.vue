<script setup>
import SidebarItem from "./SidebarItem.vue";

const exploreSection = [
  { label: "Trending", icon: "youtube-trending" },
  { label: "Music", icon: "youtube-music" },
  { label: "Movies", icon: "youtube-movies" },
  { label: "Gaming", icon: "youtube-gaming" },
  { label: "News", icon: "youtube-news" },
  { label: "Sports", icon: "youtube-sports" },
  { label: "Learning", icon: "youtube-learning" },
];
</script>

<template>
  <div class="px-10 py-1 text-left font-semibold">Explore</div>
  <ul>
    <li v-for="item in exploreSection" :key="item.label" :title="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>
