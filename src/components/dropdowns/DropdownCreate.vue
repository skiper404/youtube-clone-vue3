<script setup>
import { ref, onMounted, onUnmounted, watch } from "vue";
import DropdownCreateList from "../dropdowns/DropdownCreateList.vue";
import DropdownCreateButton from "../dropdowns/DropdownCreateButton.vue";

const menuItems = [
  { label: "Upload", icon: "user-upload" },
  { label: "Go Live", icon: "user-live" },
  { label: "Create post", icon: "user-create" },
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

function handleKeydown(event) {
  if (event.key === "Escape") {
    isOpen.value = false;
  }
}

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

onUnmounted(() => {
  window.removeEventListener("keydown", handleKeydown);
});
</script>

<template>
  <div ref="wrapper" class="relative">
    <DropdownCreateButton v-model:isOpen="isOpen" />
    <transition
      enter-active-class="transition duration-100 ease-linear"
      enter-from-class="opacity-0 scale-50 -translate-y-20"
      enter-to-class="opacity-100 scale-100 tranlate-y-0"
      leave-active-class="transition duration-100 ease-linear"
      leave-from-class="opacity-100 scale-100 -translate-y-0 "
      leave-to-class="opacity-0 -translate-y-20 scale-50"
    >
      <DropdownCreateList :menuItems="menuItems" v-if="isOpen" />
    </transition>
  </div>
</template>
