<script setup>
import TheLogo from "./TheLogo.vue";
import TheMenu from "./TheMenu.vue";

import SidebarMainSection from "./SidebarMainSection.vue";
import SidebarYouSection from "./SidebarYouSection.vue";
import SidebarSubscriptionsSection from "./SidebarSubscriptionsSection.vue";
import SidebarExploreSection from "./SidebarExploreSection.vue";
import SidebarMoreSection from "./SidebarMoreSection.vue";
import SidebarSettingsSection from "./SidebarSettingsSection.vue";
import SidebarFooterA from "./SidebarFooterA.vue";
import SidebarFooterB from "./SidebarFooterB.vue";
import SidebarCopyright from "./SidebarCopyright.vue";
</script>

<template>
  <aside
    class="fixed z-20 max-h-screen w-[260px] -translate-x-full overflow-auto bg-[#151515] transition duration-300 peer-checked:block peer-checked:translate-x-0"
  >
    <div
      class="sticky top-0 z-20 flex items-center gap-2 bg-[#111111]/95 px-6 py-2"
    >
      <TheMenu />
      <TheLogo />
    </div>
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
</template>
