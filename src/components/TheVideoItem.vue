<script setup>
import { SpeakerWaveIcon, SpeakerXMarkIcon } from "@heroicons/vue/24/outline";
import { CheckCircleIcon, EllipsisVerticalIcon } from "@heroicons/vue/24/solid";
import SubsLogo from "./icons/SubsLogo.vue";

const { title, channel } = defineProps(["index", "video"]);
</script>

<template>
  <a href="#" class="group mb-5 outline-none">
    <div class="relative">
      <img
        :src="`https://picsum.photos/seed/image${index}/560/315`"
        alt="video_preview"
        class="w-full rounded-xl"
      />
      <span
        class="absolute top-1 right-1 z-10 h-10 w-10 rounded-full bg-[#121212] p-2 opacity-0 transition duration-300 group-hover:opacity-100"
        ><SpeakerXMarkIcon
      /></span>
      <span
        class="absolute top-1 right-12 z-10 h-10 w-10 rounded-full bg-[#121212] p-2 opacity-0 transition duration-300 group-hover:opacity-100"
        ><SpeakerWaveIcon
      /></span>
      <span
        class="absolute top-12 right-1 z-10 opacity-0 transition duration-300 group-hover:opacity-100"
        ><SubsLogo
      /></span>
      <span
        class="absolute right-1 bottom-1 rounded bg-[#121212] px-0.5 text-sm font-semibold"
        >42:22</span
      >
    </div>
    <div class="mt-3 flex items-start">
      <img
        :src="`https://picsum.photos/seed/avatar${index}/32/32`"
        alt="channelLogo"
        class="mr-3 h-10 w-10 rounded-full"
      />
      <div>
        <div class="mb-1 text-left font-semibold">{{ video.title }}</div>
        <router-link
          :to="{
            name: 'Channel',
            query: {
              name: 'LEGO',
              description:
                'Here you can find a lot interestings things about LEGO!',
            },
          }"
          class="flex items-center gap-1 text-sm text-[#aaaaaa] hover:text-white"
          ><span class="">{{ video.channel }}</span>
          <CheckCircleIcon class="h-4" />
        </router-link>
        <div class="flex items-center gap-1 text-sm text-[#aaaaaa]">
          <span>{{ index + 1 }}M views</span>
          &middot;
          <span>{{ index + 1 }} month ago</span>
        </div>
      </div>
      <button class="ml-auto">
        <EllipsisVerticalIcon class="h-6" />
      </button>
    </div>
  </a>
</template>

<style lang="scss" scoped></style>
