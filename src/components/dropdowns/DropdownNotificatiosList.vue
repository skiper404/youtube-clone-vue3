<script setup>
import BaseIcon from "../BaseIcon.vue";
import DropdownNotificationListItem from "./DropdownNotificationListItem.vue";

const props = defineProps({
  notificationItems: Array,
});
</script>

<template>
  <section
    class="fixed top-12 right-18 w-[500px] rounded-2xl bg-[#242424] pb-4 text-sm"
  >
    <div class="flex items-center justify-between p-4">
      <span> Notifications </span>
      <BaseIcon name="user-settings" />
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
</template>
