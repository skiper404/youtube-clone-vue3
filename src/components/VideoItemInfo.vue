<script setup>
import { CheckCircleIcon, EllipsisVerticalIcon } from "@heroicons/vue/24/solid";
import VideoSubMenu from "./VideoSubMenu.vue";
import BaseTooltip from "./BaseTooltip.vue";

const props = defineProps({
  video: Object,
  index: Number,
  openIndex: [Number, null],
});
const { title, channel } = props.video;

const emit = defineEmits({ setOpenIndex: null });
</script>

<template>
  <div class="relative mt-3 flex items-start">
    <img
      :src="`https://picsum.photos/seed/${title}/32/32`"
      alt="channelLogo"
      class="mr-3 h-10 w-10 rounded-full"
    />
    <div>
      <div class="mb-1 text-left font-semibold" :title="title">{{ title }}</div>
      <a href="" class="flex items-center gap-1 text-[#aaaaaa]">
        <BaseTooltip :label="channel" top>
          <span>{{ channel }}</span>
        </BaseTooltip>
        <BaseTooltip label="Verified" top>
          <CheckCircleIcon class="h-4" />
        </BaseTooltip>
      </a>
      <div class="flex items-center gap-1 text-sm text-[#aaaaaa]">
        <span>{{ index + 1 }}M views</span>
        &middot;
        <span
          >{{
            `${index + 1} ${index + 1 === 1 ? "month" : "months"}`
          }}
          ago</span
        >
      </div>
    </div>

    <button class="ml-auto cursor-pointer text-gray-500 hover:text-gray-100">
      <EllipsisVerticalIcon class="h-6" @click="emit('setOpenIndex', index)" />
    </button>
    <transition
      enter-active-class="transition duration-200 ease-linear"
      enter-from-class="opacity-0 scale-0 translate-x-50 -translate-y-70"
      enter-to-class="opacity-100 scale-100 translate-x-0 translate-y-0"
      leave-active-class="transition duration-200 ease-linear"
      leave-from-class="opacity-100 scale-100 translate-x-0 -translate-y-0"
      leave-to-class="opacity-0 scale-0 translate-x-50 -translate-y-70"
    >
      <VideoSubMenu v-if="openIndex === index" />
    </transition>
  </div>
</template>
