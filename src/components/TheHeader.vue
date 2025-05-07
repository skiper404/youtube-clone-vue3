<script setup>
import SearchGroup from "./SearchGroup.vue";
import MenuLogoGroup from "./MenuLogoGroup.vue";
import DropdownGroup from "./DropdownGroup.vue";

const emit = defineEmits({ openSidebar: null });
</script>

<template>
  <header
    class="fixed top-0 right-0 left-0 z-20 flex items-center bg-[#111111]/95"
  >
    <div class="absolute inset-0 -z-10 backdrop-blur-xs"></div>
    <MenuLogoGroup @open-sidebar="emit('openSidebar')" />
    <SearchGroup />
    <DropdownGroup />
  </header>
</template>
