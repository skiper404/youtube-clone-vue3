<script setup>
import TheSearchVoice from "./TheSearchVoice.vue";
import TheSearchInput from "./TheSearchInput.vue";
</script>

<template>
  <div class="flex flex-1 items-center">
    <div
      class="mx-auto flex w-full max-w-3xl items-center justify-center gap-2 px-2"
    >
      <TheSearchInput />
      <TheSearchVoice />
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
