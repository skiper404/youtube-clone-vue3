<script setup>
import { watch, onUnmounted } from "vue";
import SidebarMainSection from "./SidebarMainSection.vue";
import SidebarYouSection from "./SidebarYouSection.vue";
import SidebarSubscriptionsSection from "./SidebarSubscriptionsSection.vue";
import SidebarExploreSection from "./SidebarExploreSection.vue";
import SidebarMoreSection from "./SidebarMoreSection.vue";
import SidebarSettingsSection from "./SidebarSettingsSection.vue";
import SidebarFooterA from "./SidebarFooterA.vue";
import SidebarFooterB from "./SidebarFooterB.vue";
import SidebarCopyright from "./SidebarCopyright.vue";
import SidebarOverlay from "./SidebarOverlay.vue";
import MenuLogoGroup from "./MenuLogoGroup.vue";

const props = defineProps({ isOpen: Boolean });
const emit = defineEmits({ closeSidebar: null });

function handleKeydown(event) {
  if (event.key === "Escape") {
    emit("closeSidebar");
  }
}

watch(
  () => props.isOpen,
  (newVal) => {
    if (newVal) {
      window.addEventListener("keydown", handleKeydown);
    } else {
      window.removeEventListener("keydown", handleKeydown);
    }
  },
);

onUnmounted(() => {
  window.removeEventListener("keydown", handleKeydown);
});
</script>

<template>
  <transition
    enter-active-class="transition-opacity duration-200 ease-linear"
    enter-from-class="opacity-0"
    enter-to-class="opacity-100"
    leave-active-class="transition-opacity duration-200 ease-linear"
    leave-from-class="opacity-100"
    leave-to-class="opacity-0"
  >
    <SidebarOverlay v-if="isOpen" @click="emit('closeSidebar')" />
  </transition>

  <transition
    enter-active-class="transition duration-200 ease-in-out transform"
    enter-from-class="-translate-x-full"
    enter-to-class="translate-x-0"
    leave-active-class="transition duration-200 ease-in-out transform"
    leave-from-class="translate-x-0"
    leave-to-class="-translate-x-full"
  >
    <aside
      v-if="isOpen"
      class="fixed z-20 max-h-screen w-[260px] overflow-auto bg-[#151515]"
    >
      <MenuLogoGroup @click="emit('closeSidebar')" />
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
  </transition>
</template>
