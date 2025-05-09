<script setup>
import { ref } from "vue";
import TheVideoItem from "./TheVideoItem.vue";

const videos = [
  { title: "You Won’t Believe What Happened!", channel: "PixelVibe" },
  { title: "Testing Weird Life Hacks", channel: "ChatterBox Daily" },
  { title: "24 Hours Without Internet", channel: "EpicEcho" },
  { title: "How I Changed My Life in a Week", channel: "WanderNest" },
  { title: "Trying This for the First Time", channel: "BrainBrew" },
  { title: "My Morning Routine 2025", channel: "ZestyZone" },
  { title: "Extreme Room Makeover", channel: "NovaNarratives" },
  { title: "What I Eat in a Day", channel: "SnackSized Stories" },
  { title: "Reacting to My Old Videos", channel: "The Curious Corner" },
  { title: "I Tried Following a Bob Ross Tutorial", channel: "GlowMode" },
  { title: "Day in the Life of a Content Creator", channel: "TrailBlaze TV" },
  { title: "Learning a New Skill in 30 Days", channel: "LoopVerse" },
  { title: "Top 10 Productivity Tips", channel: "NoodleMind" },
  { title: "Answering Your Assumptions About Me", channel: "Skyline Studio" },
  { title: "This Video Took Me 100 Hours", channel: "Binge & Beyond" },
  { title: "My Honest Thoughts on This Trend", channel: "Click & Chill" },
  { title: "Living Like a Celebrity for a Day", channel: "DreamDrop Media" },
  { title: "Things Nobody Tells You About Adulting", channel: "TurboTalks" },
  { title: "A Week Without Sugar", channel: "The Cozy Side" },
  { title: "Behind the Scenes of My Videos", channel: "Freshly Uploaded" },
  { title: "I Let Instagram Control My Day", channel: "FusionLogs" },
  { title: "Making My Own Merch!", channel: "VibeCraft" },
  { title: "This Changed Everything", channel: "ScrollStopper" },
];

const openIndex = ref(null);

const setOpenIndex = (index) => (openIndex.value = index);
</script>

<template>
  <main class="px-4 pt-30 sm:px-10 md:ml-[80px] md:px-20 xl:pl-50">
    <section
      class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3 2xl:grid-cols-4"
    >
      <TheVideoItem
        v-for="(video, index) in videos"
        :key="index"
        :index="index"
        :video="video"
        :open-index="openIndex"
        @set-open-index="setOpenIndex"
      />
    </section>
  </main>
</template>
