<script setup>
import TheMenu from "./TheMenu.vue";
import BaseTooltip from "./BaseTooltip.vue";
import YouTubeLogo from "./YouTubeLogo.vue";

const emit = defineEmits({
  openSidebar: null,
});
</script>

<template>
  <div class="sticky z-10 flex items-center gap-2 bg-[#111111]/95 px-7 py-4">
    <TheMenu @click="emit('openSidebar')" />
    <BaseTooltip label="YouTube Home">
      <a href="#">
        <YouTubeLogo class="w-28" />
      </a>
    </BaseTooltip>
  </div>
</template>
