<script setup>
import SidebarItem from "./SidebarItem.vue";

const mainSection = [
  { label: "Home", icon: "youtube-home" },
  { label: "Shorts", icon: "youtube-shorts" },
  { label: "Subscriptions", icon: "youtube-subscriptions" },
  { label: "YouTube Music", icon: "youtube-music" },
];
</script>

<template>
  <ul>
    <li v-for="item in mainSection" :key="item.label" :title="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
