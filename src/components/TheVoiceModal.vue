<script setup>
import { onBeforeUnmount, onMounted, ref, watch } from "vue";
import BaseModal from "./BaseModal.vue";
import { MicrophoneIcon } from "@heroicons/vue/24/solid";

const emit = defineEmits({ closeModal: null });

const status = ref("listening");
const timer = ref(null);

const startListeningTimer = () => {
  clearTimeout(timer.value);
  timer.value = setTimeout(() => {
    status.value = "silent";и
  }, 3000);
};

const toggleStatus = () => {
  clearTimeout(timer.value);
  status.value = status.value === "listening" ? "off" : "listening";
};

watch(
  () => status.value,
  (newStatus) => {
    if (newStatus === "listening") {
      startListeningTimer();
    }
  },
);

onMounted(() => {
  if (status.value === "listening") {
    startListeningTimer();
  }
});

onBeforeUnmount(() => clearTimeout(timer.value));
</script>

<template>
  <BaseModal @close-modal="emit('closeModal')">
    <div class="mt-10 flex px-6 text-2xl font-light text-white">
      <span v-if="status === 'listening'">Listening...</span>
      <span v-else-if="status === 'silent'">Didn't hear that. Try again.</span>
      <span v-else-if="status === 'off'">Microphone off. Try again</span>
    </div>

    <div class="relative mt-56 flex items-center justify-center">
      <span
        :class="[
          'absolute h-10 w-10 rounded-full border',
          { 'animate-ping': status === 'listening' },
        ]"
      ></span>
      <span
        :class="[
          'absolute rounded-full p-3',
          {
            'bg-red-500': status === 'listening',
            'bg-gray-400': status === 'off' || status === 'silent',
          },
        ]"
        @click="toggleStatus"
      >
        <MicrophoneIcon class="h-8" />
      </span>
      <span v-if="status !== 'listening'" class="absolute top-10 text-xs"
        >Tap microphone to try again</span
      >
    </div>
  </BaseModal>
</template>

