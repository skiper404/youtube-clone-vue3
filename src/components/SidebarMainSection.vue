<script setup>
import { HomeIcon } from "@heroicons/vue/24/solid";
import ShortsLogo from "./icons/ShortsLogo.vue";
import SubscriptionsLogo from "./icons/SubscriptionsLogo.vue";
import YouTubeMusicLogo from "./icons/YouTubeMusicLogo.vue";

import SidebarItem from "./SidebarItem.vue";

const mainSection = [
  { label: "Home", icon: HomeIcon },
  { label: "Shorts", icon: ShortsLogo },
  { label: "Subscriptions", icon: SubscriptionsLogo },
  { label: "YouTube Music", icon: YouTubeMusicLogo },
];
</script>

<template>
  <ul>
    <li v-for="item in mainSection" :key="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
