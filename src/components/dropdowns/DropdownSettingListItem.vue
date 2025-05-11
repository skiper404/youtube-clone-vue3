<script setup>
import { ChevronRightIcon } from "@heroicons/vue/24/outline";
import BaseIcon from "../BaseIcon.vue";
import { computed } from "vue";

const props = defineProps({
  label: String,
  icon: {
    type: String,
    default: "check-icon",
  },
  submenu: Boolean,
  active: Boolean,
});

const isIconShown = computed(() => props.active || props.icon !== "check-icon");
const iconName = computed(() => (props.active ? "check-icon" : props.icon));
</script>

<template>
  <a
    href="#"
    class="flex items-center gap-1 py-2 pl-2 outline-none hover:bg-[#555555]"
  >
    <BaseIcon v-if="isIconShown" class="h-6" :name="iconName" />
    <span :class="[{ 'ml-2': !active }]">{{ label }}</span>
    <ChevronRightIcon v-if="submenu" class="ml-auto h-6" />
  </a>
</template>
