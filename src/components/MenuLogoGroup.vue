<script setup>
import TheLogo from "./TheLogo.vue";
import TheMenu from "./TheMenu.vue";

const emit = defineEmits({
  openSidebar: null,
});
</script>

<template>
  <div class="sticky z-10 flex items-center gap-2 bg-[#111111]/95 px-7 py-4">
    <TheMenu @click="emit('openSidebar')" />
    <TheLogo />
  </div>
</template>
