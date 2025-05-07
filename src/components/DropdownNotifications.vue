<script setup>
import { BellIcon } from "@heroicons/vue/24/outline";

import UserSettings from "./icons/userlogos/UserSettings.vue";
import DropdownNotificationListItem from "./DropdownNotificationListItem.vue";
import { onMounted, onUnmounted, ref } from "vue";

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
</script>

<template>
  <div class="relative" ref="wrapper">
    <button
      class="rounded-full p-1 hover:bg-neutral-600"
      @click="isOpen = true"
    >
      <BellIcon class="size-7" />
    </button>
    <section
      v-if="isOpen"
      class="fixed top-12 right-18 w-[500px] rounded-2xl bg-[#242424] pb-4 text-sm"
    >
      <div class="flex items-center justify-between p-4">
        Notifications
        <UserSettings class="h-8 rounded-full p-1 hover:bg-[#555555]" />
      </div>
      <hr class="my-1 py-1 text-[#555555]" />
      <div>
        <ul class="flex flex-col divide-y divide-[#555555]">
          <li v-for="item in notificationItems" :key="item.label">
            <DropdownNotificationListItem :item="item" />
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
