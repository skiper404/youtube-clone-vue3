<script setup>
import SubMenuAddToQuery from "./icons/SubMenuAddToQuery.vue";
import SubMenuDontRecommend from "./icons/SubMenuDontRecommend.vue";
import SubMenuDownload from "./icons/SubMenuDownload.vue";
import SubMenuNotInterested from "./icons/SubMenuNotInterested .vue";
import SubMenuReport from "./icons/SubMenuReport.vue";
import SubMenuSaveToPlaylist from "./icons/SubMenuSaveToPlaylist.vue";
import SubMenuSaveToWatchLater from "./icons/SubMenuSaveToWatchLater.vue";
import SubMenuShare from "./icons/SubMenuShare.vue";

import VideoSubMenuItem from "./VideoSubMenuItem.vue";

const submenuItems = [
  { label: "Add to queue", icon: SubMenuAddToQuery },
  { label: "Save to Watch later", icon: SubMenuSaveToWatchLater },
  { label: "Save to playlist", icon: SubMenuSaveToPlaylist },
  { label: "Download", icon: SubMenuDownload },
  { label: "Share", icon: SubMenuShare },
  { label: "Not interested", icon: SubMenuNotInterested },
  { label: "Don't recommend channel", icon: SubMenuDontRecommend },
  { label: "Report", icon: SubMenuReport },
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

<style lang="scss" scoped></style>
