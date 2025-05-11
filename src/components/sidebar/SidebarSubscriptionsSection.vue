<script setup>
import { SignalIcon } from "@heroicons/vue/24/outline";

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
      :title="item.label"
      v-for="item in subscriptionsSection"
      :key="item.label"
      class="mx-4 flex items-center justify-between gap-4 rounded-xl px-2 py-1 hover:bg-[#232323]"
    >
      <div class="h-8 w-8">
        <img
          :src="`https://picsum.photos/seed/${item.label}200/200`"
          alt="video_preview"
          class="rounded-full"
        />
      </div>
      <div class="mr-auto text-sm">{{ item.label }}</div>
      <SignalIcon class="h-4 animate-pulse text-red-700" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>
