<script setup>
import { EllipsisVerticalIcon } from "@heroicons/vue/24/solid";

const props = defineProps({ item: Object });
</script>

<template>
  <a
    href="#"
    class="flex items-center justify-between gap-6 p-4 outline-none hover:bg-[#555555]"
  >
    <img
      :src="`https://picsum.photos/seed/${item.label}/200/200`"
      alt="video_preview"
      class="h-12 w-12 rounded-full"
    />
    <div class="w-70 text-left text-sm">
      <p>{{ item.label }}</p>
      <p class="font-light text-[#aaaaaa]">{{ item.release }}</p>
    </div>
    <img
      :src="`https://picsum.photos/seed/${item.release}/560/315`"
      alt="video_preview"
      class="h-9 w-16"
    />
    <button class="cursor-pointer">
      <EllipsisVerticalIcon class="h-6" />
    </button>
  </a>
</template>


