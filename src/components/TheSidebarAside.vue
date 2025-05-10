<script setup>
import SidebarSmallItem from "./SidebarAsidetem.vue";

import SidebarMainSection from "./SidebarMainSection.vue";
import SidebarYouSection from "./SidebarYouSection.vue";
import SidebarSubscriptionsSection from "./SidebarSubscriptionsSection.vue";
import SidebarExploreSection from "./SidebarExploreSection.vue";
import SidebarMoreSection from "./SidebarMoreSection.vue";
import SidebarSettingsSection from "./SidebarSettingsSection.vue";
import SidebarFooterA from "./SidebarFooterA.vue";
import SidebarFooterB from "./SidebarFooterB.vue";
import SidebarCopyright from "./SidebarCopyright.vue";

import MenuLogoGroup from "./MenuLogoGroup.vue";
const sidebarItems = [
  {
    label: "Home",
    icon: "youtube-home",
  },
  {
    label: "Shorts",
    icon: "youtube-shorts",
  },
  {
    label: "Subsriptions",
    icon: "youtube-subscriptions",
  },
  {
    label: "YouTube Music",
    icon: "youtube-music",
  },
  {
    label: "User",
    icon: "youtube-user",
  },
  {
    label: "Download",
    icon: "youtube-downloads",
  },
];
</script>

<template>
  <aside class="fixed z-10 hidden max-h-screen w-[260px] bg-[#111111] xl:block">
    <MenuLogoGroup />
    <SidebarMainSection />
    <SidebarYouSection />
    <SidebarSubscriptionsSection />
    <SidebarExploreSection />
    <SidebarMoreSection />
    <SidebarSettingsSection />
    <SidebarFooterA />
    <SidebarFooterB />
    <SidebarCopyright />
  </aside>

  <aside
    class="fixed top-14 bottom-0 left-0 z-10 mx-2 hidden w-[80px] bg-[#121212] md:block xl:hidden"
  >
    <ul>
      <li v-for="item in sidebarItems" :key="item.label">
        <SidebarSmallItem :item="item" :title="item.label" />
      </li>
    </ul>
  </aside>
</template>
