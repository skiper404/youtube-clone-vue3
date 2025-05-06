<script setup>
import TheSearchVoice from "./TheSearchVoice.vue";
import TheSearchInput from "./TheSearchInput.vue";
</script>

<template>
  <div class="flex max-w-xl flex-1 items-center justify-center gap-2 px-2">
    <input type="checkbox" id="mic" class="peer hidden" />
    <TheSearchInput />
    <TheSearchVoice />
  </div>
</template>

<style lang="scss" scoped></style>
