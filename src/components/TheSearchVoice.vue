<script setup>
import { MicrophoneIcon } from "@heroicons/vue/24/solid";
import { ref } from "vue";
import TheVoiceModal from "./TheVoiceModal.vue";

const isShowModal = ref(false);
</script>

<template>
  <div
    @click="isShowModal = true"
    ref="wrapper"
    class="flex h-10 min-w-10 items-center justify-center rounded-full bg-neutral-800 hover:bg-neutral-600 sm:flex"
  >
    <MicrophoneIcon class="size-6" />
  </div>
  <teleport to="body">
    <transition
      enter-active-class="transition duration-200 ease-linear"
      enter-from-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="transition duration-200 ease-linear"
      leave-from-class="opacity-100 "
      leave-to-class="opacity-0"
    >
      <TheVoiceModal v-if="isShowModal" @close-modal="isShowModal = false" />
    </transition>
  </teleport>
</template>
