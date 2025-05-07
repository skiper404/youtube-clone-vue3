<script setup>
import { CheckCircleIcon, EllipsisVerticalIcon } from "@heroicons/vue/24/solid";

const props = defineProps({ video: Object, index: Number });
const { title, channel } = props.video;
</script>

<template>
  <div class="mt-3 flex items-start">
    <img
      :src="`https://picsum.photos/seed/${title}/32/32`"
      alt="channelLogo"
      class="mr-3 h-10 w-10 rounded-full"
    />
    <div>
      <div class="mb-1 text-left font-semibold">{{ title }}</div>
      <a href="" class="">
        <span class="">{{ channel }}</span>
        <CheckCircleIcon class="h-4" />
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
    <button class="ml-auto">
      <EllipsisVerticalIcon class="h-6" />
    </button>
  </div>
</template>

<style lang="scss" scoped></style>
