<script setup>
import SidebarItem from "./SidebarItem.vue";

const settingsSection = [
  { label: "Setting", icon: "youtube-settings" },
  { label: "Report history", icon: "youtube-history" },
  { label: "Help", icon: "youtube-help" },
  { label: "Send feedback", icon: "youtube-feedback" },
];
</script>

<template>
  <ul>
    <li v-for="item in settingsSection" :key="item.label" :title="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
