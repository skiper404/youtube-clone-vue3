<script setup>
import VideoItemInfo from "./VideoItemInfo.vue";
import VideoItemThumbnail from "./VideoItemThumbnail.vue";
const props = defineProps({
  index: Number,
  video: Object,
  openIndex: [Number, null],
});

const emit = defineEmits({ setOpenIndex: null });
</script>

<template>
  <a class="group mb-5 outline-none">
    <VideoItemThumbnail :index="index" />
    <VideoItemInfo
      :video="video"
      :index="index"
      :open-index="openIndex"
      @set-open-index="emit('setOpenIndex', $event)"
    />
  </a>
</template>
