<script setup>
import { SpeakerWaveIcon, SpeakerXMarkIcon } from "@heroicons/vue/24/outline";
import SubsLogo from "./icons/SubsLogo.vue";

const props = defineProps({ index: Number });
</script>

<template>
  <div class="relative">
    <img
      :src="`https://picsum.photos/seed/${index + 1}/560/315`"
      alt="video_preview"
      class="w-full rounded-xl"
    />
    <span
      class="absolute top-1 right-1 z-10 h-10 w-10 rounded-full bg-[#121212] p-2 opacity-0 transition duration-300 group-hover:opacity-100"
      ><SpeakerXMarkIcon />
    </span>
    <span
      class="absolute top-1 right-12 z-10 h-10 w-10 rounded-full bg-[#121212] p-2 opacity-0 transition duration-300 group-hover:opacity-100"
      ><SpeakerWaveIcon />
    </span>
    <span
      class="absolute top-12 right-1 z-10 opacity-0 transition duration-300 group-hover:opacity-100"
    >
      <SubsLogo />
    </span>
    <span
      class="absolute right-1 bottom-1 rounded bg-[#121212] px-0.5 text-sm font-semibold"
      >{{
        index.toString().padStart(2, 1) + ":" + index.toString().padStart(2, 1)
      }}
    </span>
  </div>
</template>

<style lang="scss" scoped></style>
