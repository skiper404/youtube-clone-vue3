<script setup>
import SidebarItem from "./SidebarItem.vue";

import YouTubeSettingsLogo from "./icons/YouTubeSettingsLogo.vue";
import ReportHistoryLogo from "./icons/ReportHistoryLogo.vue";
import HelpLogo from "./icons/HelpLogo.vue";
import SendFeedbackLogo from "./icons/SendFeedbackLogo.vue";

const settingsSection = [
  { label: "Setting", icon: YouTubeSettingsLogo },
  { label: "Report history", icon: ReportHistoryLogo },
  { label: "Help", icon: HelpLogo },
  { label: "Send feedback", icon: SendFeedbackLogo },
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
