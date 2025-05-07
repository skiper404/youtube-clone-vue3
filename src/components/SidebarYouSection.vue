<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/solid";
import HistoryLogo from "./icons/HistoryLogo.vue";
import PlaylistLogo from "./icons/PlaylistLogo.vue";
import YourVideosLogo from "./icons/YourVideosLogo.vue";
import WatchLaterLogo from "./icons/WatchLaterLogo.vue";
import LikedVideosLogo from "./icons/LikedVideosLogo.vue";
import DownloadsLogo from "./icons/DownloadsLogo.vue";

import SidebarItem from "./SidebarItem.vue";

const youSection = [
  { label: "You", icon: ChevronRightIcon },
  { label: "History", icon: HistoryLogo },
  { label: "Playlists", icon: PlaylistLogo },
  { label: "Your videos", icon: YourVideosLogo },
  { label: "Watch later", icon: WatchLaterLogo },
  { label: "Liked videos", icon: LikedVideosLogo },
  { label: "Downloads", icon: DownloadsLogo },
];
</script>

<template>
  <ul>
    <li v-for="item in youSection" :key="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
