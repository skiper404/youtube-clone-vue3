<script setup>
import { EllipsisVerticalIcon } from "@heroicons/vue/24/solid";

const props = defineProps(["item"]);
const { label, release } = props.item;
</script>

<template>
  <a
    href="#"
    class="flex items-center justify-between gap-6 p-4 outline-none hover:bg-[#555555]"
  >
    <img
      :src="`https://picsum.photos/seed/${label}/560/315`"
      alt="video_preview"
      class="h-12 w-12 rounded-full"
    />
    <div class="w-70 text-left text-sm">
      <p>{{ label }}</p>
      <p class="font-light text-[#aaaaaa]">{{ release }}</p>
    </div>
    <img
      :src="`https://picsum.photos/seed/${release}/560/315`"
      alt="video_preview"
      class="h-9 w-16"
    />
    <button class="">
      <EllipsisVerticalIcon class="h-6" />
    </button>
  </a>
</template>

<style lang="scss" scoped></style>
