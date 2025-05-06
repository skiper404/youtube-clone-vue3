<script setup>
import {
  Bars3Icon,
  ChevronRightIcon,
  ChevronDownIcon,
} from "@heroicons/vue/24/outline";

import YouTubeLogo from "./icons/YouTubeLogo.vue";
import HomeLogo from "./icons/HomeLogo.vue";
import ShortsLogo from "./icons/ShortsLogo.vue";
import SubscriptionsLogo from "./icons/SubscriptionsLogo.vue";
import YouTubeMusicLogo from "./icons/YouTubeMusicLogo.vue";
import HistoryLogo from "./icons/HistoryLogo.vue";
import PlaylistLogo from "./icons/PlaylistLogo.vue";
import YourVideosLogo from "./icons/YourVideosLogo.vue";
import WatchLaterLogo from "./icons/WatchLaterLogo.vue";
import LikedVideosLogo from "./icons/LikedVideosLogo.vue";
import DownloadsLogo from "./icons/DownloadsLogo.vue";
import TrendingLogo from "./icons/TrendingLogo.vue";
import MusicLogo from "./icons/MusicLogo.vue";
import MoviesLogo from "./icons/MoviesLogo.vue";
import GamingLogo from "./icons/GamingLogo.vue";
import NewsLogo from "./icons/NewsLogo.vue";
import SportsLogo from "./icons/SportsLogo.vue";
import LearningLogo from "./icons/LearningLogo.vue";
import YouTubeStudioRed from "./icons/YouTubeStudioRed.vue";
import YouTubeMusicLogoRed from "./icons/YouTubeMusicLogoRed.vue";
import YouTubeKidsLogoRed from "./icons/YouTubeKidsLogoRed.vue";
import YouTubeSettingsLogo from "./icons/YouTubeSettingsLogo.vue";
import ReportHistoryLogo from "./icons/ReportHistoryLogo.vue";
import HelpLogo from "./icons/HelpLogo.vue";
import SendFeedbackLogo from "./icons/SendFeedbackLogo.vue";
</script>

<template>
  <aside
    class="fixed z-20 max-h-screen w-[260px] -translate-x-full overflow-auto bg-[#151515] transition duration-300 peer-checked:block peer-checked:translate-x-0"
  >
    <nav>
      <div
        class="sticky top-0 z-20 flex items-center gap-2 bg-[#111111] px-6 py-2"
      >
        <input id="toggle-menu" type="checkbox" class="peer hidden" />
        <label for="toggle-menu" class="cursor-pointer p-1">
          <Bars3Icon class="h-7" />
        </label>
        <a href="#" class="w-32 cursor-pointer py-2 pr-5 outline-none">
          <YouTubeLogo />
        </a>
      </div>

      <ul>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl bg-[#232323] px-6 py-2 text-sm outline-none"
            ><HomeLogo class="h-6" />Home</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ShortsLogo class="h-6" />Shorts</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <SubscriptionsLogo class="h-6" />Subscriptions<span
              class="h-1 w-1 rounded-full bg-blue-400"
            ></span
          ></a>
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><YouTubeMusicLogo class="h-6" />YouTube Music</a
          >
        </li>
      </ul>
      <hr class="m-2 border-1 border-[#373737]" />
      <ul>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-4 rounded-xl px-6 py-2 text-sm font-semibold outline-none hover:bg-[#232323] focus:bg-[#232323]"
            >You<ChevronRightIcon class="h-6"
          /></a>
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><HistoryLogo class="h-6" />History</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <PlaylistLogo class="h-6" />Playlists</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><YourVideosLogo class="h-6" />Your videos</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <WatchLaterLogo class="h-6" />Watch later</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <LikedVideosLogo class="h-6" />Liked videos</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <DownloadsLogo class="h-6" />Downloads</a
          >
        </li>
      </ul>
      <hr class="m-2 border-1 border-[#373737]" />
      <div class="px-10 py-1 text-left font-semibold">Subscriptions</div>
      <ul>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="A" color="#0042a9" />Video 1</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="B" color="#4382D3" />Video 2</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="N" color="#238223" />Video 3</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="D" color="#13D2A3" />Video 4</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="S" color="#432223" />Video 5</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="W" color="#13A273" />Video 6</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="B" color="#432273" />Video 7</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChannelLogo letter="Si" color="#228251" />Video 8</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ChevronDownIcon class="h-6" />Show more</a
          >
        </li>
      </ul>
      <hr class="m-2 border-1 border-[#373737]" />
      <div class="px-10 py-1 text-left font-semibold">Explore</div>
      <ul>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><TrendingLogo class="h-6" />Trending</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><MusicLogo class="h-6" />Music</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><MoviesLogo class="h-6" />Movies</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><GamingLogo class="h-6" />Gaming</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><NewsLogo class="h-6" />News</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <SportsLogo class="h-6" />Sports</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <LearningLogo class="h-6" />Learning</a
          >
        </li>
      </ul>
      <hr class="m-2 border-1 border-[#373737]" />
      <div class="px-10 py-1 text-left font-semibold">More from YouTube</div>
      <ul>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <YouTubeStudioRed class="h-6" />YouTube Studio</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <YouTubeMusicLogoRed class="h-6" />YouTube Music</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><YouTubeKidsLogoRed class="h-6" />YouTube Kids</a
          >
        </li>
      </ul>
      <hr class="m-2 border-1 border-[#373737]" />
      <ul>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
          >
            <YouTubeSettingsLogo class="h-6" />Setting</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><ReportHistoryLogo class="h-6" />Report history</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><HelpLogo class="h-6" />Help</a
          >
        </li>
        <li class="px-4">
          <a
            href="#"
            class="flex items-center gap-6 rounded-xl px-6 py-2 text-sm outline-none hover:bg-[#232323] focus:bg-[#232323]"
            ><SendFeedbackLogo class="h-6" />Send feedback</a
          >
        </li>
      </ul>
      <hr class="m-2 border-1 border-[#373737]" />
      <ul
        class="flex flex-wrap gap-1 px-8 pt-4 text-xs font-semibold text-[#aaaaaa]"
      >
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">About</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Press</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Copyright</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Contact us</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Creators</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Advertise</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Developers</a>
        </li>
      </ul>
      <ul
        class="flex flex-wrap gap-1 px-8 pt-4 text-xs font-semibold text-[#aaaaaa]"
      >
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Terms</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]">Privacy</a>
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]"
            >Policy & Safety</a
          >
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]"
            >How YouTube works</a
          >
        </li>
        <li>
          <a href="#" class="p-1 outline-none focus:bg-[#232323]"
            >Test new features</a
          >
        </li>
      </ul>
      <a
        href="#"
        class="m-2 block px-8 text-left text-xs font-semibold text-[#717171] outline-none"
        >&copy; 2025 Google LLC</a
      >
    </nav>
  </aside>
</template>
