<script setup>
import SidebarItem from "./SidebarItem.vue";

const subscriptionsSection = [
  { label: "TechFlow" },
  { label: "Daily Vibes" },
  { label: "FoodTrip TV" },
  { label: "GameMasterX" },
  { label: "CodeWithMax" },
  { label: "Travelista" },
  { label: "ZenMusic" },
];
</script>

<template>
  <div class="px-10 py-1 text-left font-semibold">Subscriptions</div>
  <ul>
    <li
      v-for="item in subscriptionsSection"
      :key="item.label"
      class="mx-4 flex items-center rounded-xl px-2 py-1 hover:bg-[#232323]"
    >
      <img
        :src="`https://picsum.photos/seed/${item.label}200/200`"
        alt="video_preview"
        class="h-8 w-8 rounded-full"
      />
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
