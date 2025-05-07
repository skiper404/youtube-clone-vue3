<script setup>
import VideoItemInfo from "./VideoItemInfo.vue";
import VideoItemThumbnail from "./VideoItemThumbnail.vue";
const props = defineProps({ index: Number, video: Object });
</script>

<template>
  <a href="#" class="group mb-5 outline-none">
    <VideoItemThumbnail :index="index" />
    <VideoItemInfo :video="video" :index="index" />
  </a>
</template>
