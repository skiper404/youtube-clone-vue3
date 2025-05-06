<script setup>
import { XMarkIcon } from "@heroicons/vue/24/outline";
import { MicrophoneIcon } from "@heroicons/vue/24/solid";
</script>

<template>
  <label for="mic" class="cursor-pointer">
    <div
      class="flex min-h-10 min-w-10 items-center justify-center rounded-full bg-neutral-800 hover:bg-neutral-600 sm:flex"
    >
      <MicrophoneIcon class="size-6" />
    </div>
  </label>
  <label
    for="mic"
    class="fixed inset-0 z-10 hidden cursor-pointer justify-center bg-black/50 peer-checked:flex"
  >
    <div class="relative mt-10 h-[400px] w-[500px] rounded-xl bg-[#242424] p-4">
      <button
        for="mic"
        class="absolute top-4 right-4 cursor-pointer px-3 py-1 hover:bg-neutral-700"
      >
        <XMarkIcon class="h-10" />
      </button>
      <p class="mt-10 px-10 text-left text-3xl text-white">Listening...</p>
      <div
        class="absolute bottom-10 left-54 animate-ping rounded-full bg-red-500 p-3"
      >
        <MicrophoneIcon class="size-6" />
      </div>
    </div>
  </label>
</template>

<style lang="scss" scoped></style>
