<script setup>
import VideoSubMenuItem from "./VideoSubMenuItem.vue";

const submenuItems = [
  { label: "Add to queue", icon: "youtube-submenu-add" },
  { label: "Save to Watch later", icon: "youtube-submenu-watch-later" },
  { label: "Save to playlist", icon: "youtube-submenu-playlist" },
  { label: "Download", icon: "youtube-submenu-downloads" },
  { label: "Share", icon: "youtube-submenu-share" },
  { label: "Not interested", icon: "youtube-submenu-not-interested" },
  {
    label: "Don't recommend channel",
    icon: "youtube-submenu-don't-recommended",
  },
  { label: "Report", icon: "youtube-submenu-report" },
];
</script>

<template>
  <div class="absolute top-10 right-0 z-10 mx-2 rounded-xl bg-[#333333] py-2">
    <ul>
      <li v-for="item in submenuItems" :key="item.label">
        <VideoSubMenuItem :item="item" />
      </li>
    </ul>
  </div>
</template>

