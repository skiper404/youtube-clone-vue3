<script setup>
import { XMarkIcon, MagnifyingGlassIcon } from "@heroicons/vue/24/outline";
</script>

<template>
  <form class="relative flex w-full items-center">
    <input
      type="text"
      class="w-full rounded-l-full border border-neutral-800 px-4 py-2 outline-0 focus:border-blue-500"
      placeholder="Search"
    />
    <button type="button" class="absolute top-0 right-16">
      <XMarkIcon class="h-10 p-1" />
    </button>
    <button
      type="submit"
      class="rounded-r-full border border-neutral-800 bg-neutral-800 px-4 py-2 hover:bg-neutral-600"
    >
      <MagnifyingGlassIcon class="h-6" />
    </button>
  </form>
</template>

<style lang="scss" scoped></style>
