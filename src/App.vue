<script setup>
import TheHeader from "./components/TheHeader.vue";
import TheSidebarAside from "./components/TheSidebarAside.vue";
import TheSidebar from "./components/TheSidebar.vue";
import TheCategories from "./components/TheCategories.vue";
import TheVideos from "./components/TheVideos.vue";
import { ref } from "vue";

const isOpen = ref(false);
const openSidebar = () => (isOpen.value = true);
const closeSidebar = () => (isOpen.value = false);
</script>

<template>
  <TheHeader @open-sidebar="openSidebar" />
  <TheSidebarAside />
  <TheSidebar :is-open="isOpen" @close-sidebar="closeSidebar" />
  <TheCategories />
  <TheVideos />
</template>
