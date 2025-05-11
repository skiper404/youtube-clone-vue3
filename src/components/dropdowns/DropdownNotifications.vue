<script setup>
import { onMounted, onUnmounted, ref, watch } from "vue";
import DropdownNotificationsButton from "./DropdownNotificationsButton.vue";
import DropdownNotificatiosList from "./DropdownNotificatiosList.vue";

const notificationItems = [
  { label: "Arthas is live: Последний из вас", release: "1 day ago" },
  {
    label: "Bouleward Depo uploaded: Bouleward Depo - ДЫРБУЛЩИЩ",
    release: "3 days ago",
  },
  {
    label: "Янчик uploaded: Пересадка",
    release: "4 days ago",
  },
  {
    label: "Paul_Matteo uploaded: Тот самый друг",
    release: "5 days ago",
  },
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

onUnmounted(() => {
  window.removeEventListener("keydown", handleKeydown);
});

const handleKeydown = (event) => {
  if (event.key === "Escape") {
    isOpen.value = false;
  }
};

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
</script>

<template>
  <div class="relative" ref="wrapper">
    <DropdownNotificationsButton v-model:isOpen="isOpen" />
    <transition
      enter-active-class="transition duration-100 ease-linear"
      enter-from-class="opacity-0 scale-50 -translate-y-20"
      enter-to-class="opacity-100 scale-100 tranlate-y-0"
      leave-active-class="transition duration-100 ease-linear"
      leave-from-class="opacity-100 scale-100 -translate-y-0 "
      leave-to-class="opacity-0 -translate-y-20 scale-50"
    >
      <DropdownNotificatiosList
        v-if="isOpen"
        :notificationItems="notificationItems"
      />
    </transition>
  </div>
</template>
