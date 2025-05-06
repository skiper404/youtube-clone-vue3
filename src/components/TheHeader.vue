<script setup>
import TheDropdownSettings from "./TheDropdownSettings.vue";
import TheDropdownNotifications from "./TheDropdownNotifications.vue";
import TheDropdownCreate from "./TheDropdownCreate.vue";
import TheSearch from "./TheSearch.vue";
import TheLogo from "./TheLogo.vue";
import TheMenu from "./TheMenu.vue";
</script>

<template>
  <input id="toggle-menu" type="checkbox" class="peer hidden" />
  <header
    class="fixed top-0 right-0 left-0 z-20 flex bg-[#111111]/95 px-6 py-2"
  >
    <div class="absolute inset-0 -z-1 backdrop-blur-xs"></div>

    <div class="flex items-center justify-center gap-2">
      <TheMenu />
      <TheLogo />
    </div>

    <div class="flex flex-1 justify-center">
      <TheSearch />
    </div>

    <div class="hidden items-center justify-center gap-2 sm:flex">
      <TheDropdownCreate />
      <TheDropdownNotifications />
      <TheDropdownSettings />
    </div>
  </header>
</template>
