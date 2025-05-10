<script setup>
import { SpeakerWaveIcon, SpeakerXMarkIcon } from "@heroicons/vue/24/outline";
import BaseIcon from "./BaseIcon.vue";

import { ref } from "vue";

const props = defineProps({ index: Number });

const enableSound = ref(false);
const enableSubtitles = ref(true);
</script>

<template>
  <div class="relative">
    <img
      :src="`https://picsum.photos/seed/${index + 1}/560/315`"
      alt="video_preview"
      class="w-full rounded-xl"
    />
    <span
      v-if="enableSound"
      @click="enableSound = false"
      class="absolute top-1 right-1 z-10 h-10 w-10 scale-0 rounded-full bg-[#121212]/70 p-2 opacity-0 transition duration-300 group-hover:scale-100 group-hover:opacity-100"
      ><SpeakerXMarkIcon />
    </span>
    <span
      v-if="!enableSound"
      @click="enableSound = true"
      class="absolute top-1 right-1 z-10 h-10 w-10 scale-0 rounded-full bg-[#121212]/70 p-2 opacity-0 transition duration-300 group-hover:scale-100 group-hover:opacity-100"
      ><SpeakerWaveIcon />
    </span>
    <span
      v-if="!enableSubtitles"
      @click="enableSubtitles = true"
      class="absolute top-12 right-1 z-10 h-10 w-10 scale-0 rounded-full bg-[#121212]/70 p-2 opacity-0 transition duration-300 group-hover:scale-100 group-hover:opacity-100"
    >
      <BaseIcon name="subs-logo-off" />
    </span>
    <span
      v-if="enableSubtitles"
      @click="enableSubtitles = false"
      class="absolute top-12 right-1 z-10 h-10 w-10 scale-0 rounded-full bg-[#121212]/70 p-2 opacity-0 transition duration-300 group-hover:scale-100 group-hover:opacity-100"
    >
      <BaseIcon name="subs-logo-on" />
    </span>
    <span
      class="absolute right-1 bottom-1 rounded bg-[#121212]/70 px-0.5 text-sm font-semibold"
      >{{
        index.toString().padStart(2, 1) + ":" + index.toString().padStart(2, 1)
      }}
    </span>
  </div>
</template>

<style lang="scss" scoped></style>
