<script setup>
import TheSearchVoice from "./TheSearchVoice.vue";
import TheSearchInput from "./TheSearchInput.vue";
import BaseTooltip from "./BaseTooltip.vue";
</script>

<template>
  <div class="flex flex-1 items-center">
    <div
      class="mx-auto flex w-full max-w-3xl items-center justify-center gap-2 px-2"
    >
      <TheSearchInput />
      <BaseTooltip label="Search with voice">
        <TheSearchVoice class="border" />
      </BaseTooltip>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
