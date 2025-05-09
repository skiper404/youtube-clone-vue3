<script setup>
import { PlusIcon } from "@heroicons/vue/24/outline";
import UserUpload from "./icons/userlogos/UserUpload.vue";
import UserCrearePost from "./icons/userlogos/UserCrearePost.vue";
import UserLive from "./icons/userlogos/UserLive.vue";
import DropdownCreateListItem from "./DropdownCreateListItem.vue";
import { ref, onMounted, onUnmounted, watch } from "vue";

const menuItems = [
  { label: "Upload", icon: UserUpload },
  { label: "Go Live", icon: UserLive },
  { label: "Create post", icon: UserCrearePost },
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
    <button
      class="flex h-10 items-center justify-center gap-2 rounded-full bg-neutral-800 px-3 hover:bg-neutral-600"
      @click="isOpen = true"
    >
      <PlusIcon class="size-6" />
      <span class="text-sm font-semibold">Create</span>
    </button>

    <transition
      enter-active-class="transition duration-100 ease-linear"
      enter-from-class="opacity-0 scale-50 -translate-y-20"
      enter-to-class="opacity-100 scale-100 tranlate-y-0"
      leave-active-class="transition duration-100 ease-linear"
      leave-from-class="opacity-100 scale-100 -translate-y-0 "
      leave-to-class="opacity-0 -translate-y-20 scale-50"
    >
      <section
        v-if="isOpen"
        class="fixed top-10 right-4 w-[200px] rounded-xl bg-[#242424]"
      >
        <ul class="my-2 rounded-xl text-sm">
          <li
            class="py-2 hover:bg-[#555555]"
            v-for="item in menuItems"
            :key="item.label"
          >
            <DropdownCreateListItem :item="item" />
          </li>
        </ul>
      </section>
    </transition>
  </div>
</template>

<style lang="scss" scoped></style>
