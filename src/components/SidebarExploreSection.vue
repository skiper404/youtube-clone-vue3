<script setup>
import TrendingLogo from "./icons/TrendingLogo.vue";
import MusicLogo from "./icons/MusicLogo.vue";
import MoviesLogo from "./icons/MoviesLogo.vue";
import GamingLogo from "./icons/GamingLogo.vue";
import NewsLogo from "./icons/NewsLogo.vue";
import SportsLogo from "./icons/SportsLogo.vue";
import LearningLogo from "./icons/LearningLogo.vue";

import SidebarItem from "./SidebarItem.vue";

const exploreSection = [
  { label: "Trending", icon: TrendingLogo },
  { label: "Music", icon: MusicLogo },
  { label: "Movies", icon: MoviesLogo },
  { label: "Gaming", icon: GamingLogo },
  { label: "News", icon: NewsLogo },
  { label: "Sports", icon: SportsLogo },
  { label: "Learning", icon: LearningLogo },
];
</script>

<template>
  <div class="px-10 py-1 text-left font-semibold">Explore</div>
  <ul>
    <li v-for="item in exploreSection" :key="item.label">
      <SidebarItem :item="item" />
    </li>
  </ul>
  <hr class="m-2 border-1 border-[#373737]" />
</template>

<style lang="scss" scoped></style>
