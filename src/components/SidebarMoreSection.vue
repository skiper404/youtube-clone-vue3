<script setup>
import YouTubeStudioRed from "./icons/YouTubeStudioRed.vue";
import YouTubeMusicLogoRed from "./icons/YouTubeMusicLogoRed.vue";
import YouTubeKidsLogoRed from "./icons/YouTubeKidsLogoRed.vue";

import SidebarItem from "./SidebarItem.vue";

const moreSection = [
  { label: "YouTube Studio", icon: YouTubeStudioRed },
  { label: "YouTube Music", icon: YouTubeMusicLogoRed },
  { label: "YouTube Kids", icon: YouTubeKidsLogoRed },
];
</script>

<template>
  <div class="px-10 py-1 text-left font-semibold">More from YouTube</div>
  <ul>
    <li v-for="item in moreSection" :key="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
