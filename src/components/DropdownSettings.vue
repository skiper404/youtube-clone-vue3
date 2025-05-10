<script setup>
import DropdownSettingListItem from "./DropdownSettingListItem.vue";
import { onUnmounted, ref, onMounted, watch } from "vue";

const settingItems = [
  { label: "Google Account", icon: "user-google" },
  { label: "Switch Account", icon: "user-switch" },
  { label: "Sign out", icon: "user-signout" },
  { label: "YouTube studio", icon: "user-studio" },
  { label: "Your Premium Benefits", icon: "user-premium" },
  { label: "Purchases and memberships", icon: "user-purchase" },
  { label: "Your data in YouTube", icon: "user-data" },
  { label: "Appearence: Device theme", icon: "user-apperiance" },
  { label: "Restricted Mode: Off", icon: "user-mode" },
  { label: "Language: English", icon: "user-language" },
  { label: "Location: Ukraine", icon: "user-location" },
  { label: "Keyboard shortcuts", icon: "user-keyboard" },
  { label: "Settings", icon: "user-settings" },
  { label: "Help", icon: "user-help" },
  { label: "Send feedback", icon: "user-feedback" },
];

const isOpen = ref(false);
const wrapper = ref(null);

const handleClickOutside = (event) => {
  if (wrapper.value && !wrapper.value.contains(event.target)) {
    isOpen.value = false;
  }
};

onMounted(() => window.addEventListener("click", handleClickOutside));
onUnmounted(() => window.removeEventListener("click", handleClickOutside));

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
  <div class="relative" ref="wrapper">
    <img
      :src="`https://picsum.photos/200/200`"
      alt="video_preview"
      class="mr-2 h-10 w-10 rounded-full"
      @click="isOpen = true"
    />
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
      class="fixed top-12 right-4 w-[300px] overflow-auto rounded-2xl bg-[#242424] peer-checked:block"
    >
      <div class="mx-2 flex">
        <img
          :src="`https://picsum.photos/500/500`"
          alt="video_preview"
          class="m-2 h-10 w-10 rounded-full"
        />
        <div class="flex flex-col items-start py-2">
          <span>John Doe</span>
          <span>@Joundoe12</span>
          <a href="#" class="cursor-pointer py-1 text-blue-400 outline-none"
            >View your channel</a
          >
        </div>
      </div>
      <hr class="my-1 py-1 text-[#555555]" />
      <ul class="text-sm">
        <li v-for="item in settingItems" :key="item.label">
          <DropdownSettingListItem :item="item" />
        </li>
      </ul>
    </section>
  </transition>
</template>

<style lang="scss" scoped></style>
