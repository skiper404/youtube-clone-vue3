<script setup>
import { XMarkIcon } from "@heroicons/vue/24/outline";
import { MicrophoneIcon } from "@heroicons/vue/24/solid";
import { onMounted, onUnmounted, ref, watch } from "vue";

const isOpen = ref(false);
const wrapper = ref(null);

const handleClickOutline = (event) => {
  if (wrapper.value && !wrapper.value.contains(event.target)) {
    isOpen.value = false;
  }
};

onMounted(() => window.addEventListener("click", handleClickOutline));
onUnmounted(() => window.removeEventListener("click", handleClickOutline));

function handleKeydown(event) {
  if (event.key === "Escape") {
    isOpen.value = false;
  }
}

watch(
  () => isOpen.value,
  (newVal) => {
    if (newVal) {
      window.addEventListener("keydown", handleKeydown);
    } else {
      window.removeEventListener("keydown", handleKeydown);
    }
  },
);

onUnmounted(() => {
  window.removeEventListener("keydown", handleKeydown);
});
</script>

<template>
  <div
    @click="isOpen = true"
    ref="wrapper"
    class="flex h-10 min-w-10 items-center justify-center rounded-full bg-neutral-800 hover:bg-neutral-600 sm:flex"
  >
    <MicrophoneIcon class="size-6" />
  </div>
  <transition
    enter-active-class="transition duration-100 ease-linear"
    enter-from-class="opacity-0 scale-50 -translate-y-20"
    enter-to-class="opacity-100 scale-100 tranlate-y-0"
    leave-active-class="transition duration-100 ease-linear"
    leave-from-class="opacity-100 scale-100 -translate-y-0 "
    leave-to-class="opacity-0 -translate-y-20 scale-50"
  >
    <section
      v-if="isOpen"
      class="fixed inset-0 z-10 cursor-pointer justify-center bg-black/50"
    >
      <div
        class="relative mx-auto mt-10 flex h-[400px] w-[500px] rounded-xl bg-[#242424] p-4"
      >
        <button
          class="absolute top-4 right-4 cursor-pointer rounded-full hover:bg-neutral-700"
          @click="isOpen = false"
        >
          <XMarkIcon class="h-10" />
        </button>
        <div class="px-10 text-left text-3xl text-white">Listening...</div>

        <div
          class="absolute bottom-10 left-54 animate-ping rounded-full bg-red-500 p-3"
        >
          <MicrophoneIcon class="size-6" />
        </div>
      </div>
    </section>
  </transition>
</template>

<style lang="scss" scoped></style>
