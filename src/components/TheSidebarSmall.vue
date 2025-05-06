<script setup>
import { UserCircleIcon } from "@heroicons/vue/24/outline";

import HomeLogo from "./icons/HomeLogo.vue";
import ShortsLogo from "./icons/ShortsLogo.vue";
import SubscriptionsLogo from "./icons/SubscriptionsLogo.vue";
import YouTubeMusicLogo from "./icons/YouTubeMusicLogo.vue";

import DownloadsLogo from "./icons/DownloadsLogo.vue";
</script>

<template>
  <aside
    class="fixed top-14 bottom-0 left-0 z-20 hidden w-[80px] bg-[#111111] md:block"
  >
    <nav>
      <ul class="flex flex-col items-center gap-3 text-[10px]">
        <li class="w-full">
          <a
            href="#"
            class="flex flex-col gap-1 rounded-lg py-2 outline-none hover:bg-[#292929] focus:bg-[#292929]"
            ><HomeLogo class="h-6" />Home
          </a>
        </li>
        <li class="w-full">
          <a
            href="#"
            class="flex flex-col gap-1 rounded-lg py-2 outline-none hover:bg-[#292929] focus:bg-[#292929]"
            ><ShortsLogo class="h-6" />Shorts</a
          >
        </li>
        <li class="w-full">
          <a
            href="#"
            class="flex flex-col gap-1 rounded-lg py-2 outline-none hover:bg-[#292929] focus:bg-[#292929]"
            ><SubscriptionsLogo class="h-6" />Subscriptions
          </a>
        </li>
        <li class="w-full">
          <a
            href="#"
            class="flex flex-col gap-1 rounded-lg py-2 outline-none hover:bg-[#292929] focus:bg-[#292929]"
            ><YouTubeMusicLogo class="h-6" />YouTube Music</a
          >
        </li>
        <li class="w-full">
          <a
            href="#"
            class="flex flex-col gap-1 rounded-lg py-2 outline-none hover:bg-[#292929] focus:bg-[#292929]"
            ><UserCircleIcon class="h-6" />You</a
          >
        </li>
        <li class="w-full">
          <a
            href="#"
            class="flex flex-col gap-1 rounded-lg py-2 outline-none hover:bg-[#292929] focus:bg-[#292929]"
            ><DownloadsLogo class="h-6" />Downloads</a
          >
        </li>
      </ul>
    </nav>
  </aside>
</template>
