<script setup>
import { UserCircleIcon } from "@heroicons/vue/24/outline";
import HomeLogo from "./icons/HomeLogo.vue";
import ShortsLogo from "./icons/ShortsLogo.vue";
import SubscriptionsLogo from "./icons/SubscriptionsLogo.vue";
import YouTubeMusicLogo from "./icons/YouTubeMusicLogo.vue";
import DownloadsLogo from "./icons/DownloadsLogo.vue";
import SidebarSmallItem from "./SidebarSmallItem.vue";

const sidebarItems = [
  {
    label: "Download",
    icon: HomeLogo,
  },
  {
    label: "Shorts",
    icon: ShortsLogo,
  },
  {
    label: "Subsriptions",
    icon: SubscriptionsLogo,
  },
  {
    label: "YouTube Music",
    icon: YouTubeMusicLogo,
  },
  {
    label: "User",
    icon: UserCircleIcon,
  },
  {
    label: "Download",
    icon: DownloadsLogo,
  },
];
</script>

<template>
  <aside
    class="fixed top-14 bottom-0 left-0 z-20 hidden w-[80px] bg-[#111111] md:block"
  >
    <nav>
      <ul>
        <li v-for="item in sidebarItems" :key="item.label">
          <SidebarSmallItem :item="item" />
        </li>
      </ul>
    </nav>
  </aside>
</template>
