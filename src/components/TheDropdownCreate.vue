<script setup>
import { PlusIcon } from "@heroicons/vue/24/outline";
import UserUpload from "./icons/userlogos/UserUpload.vue";
import UserCrearePost from "./icons/userlogos/UserCrearePost.vue";
import UserLive from "./icons/userlogos/UserLive.vue";
import DropdownCreateListItem from "./DropdownCreateListItem.vue";

const menuItems = [
  { label: "Upload", icon: UserUpload },
  { label: "Go Live", icon: UserLive },
  { label: "Create post", icon: UserCrearePost },
];
</script>

<template>
  <div class="flex">
    <input type="checkbox" id="createBlock" class="peer hidden" />
    <label for="createBlock">
      <div
        class="flex h-10 items-center justify-center gap-2 rounded-full bg-neutral-800 px-3 hover:bg-neutral-600"
      >
        <PlusIcon class="size-6" />
        <span class="text-sm font-semibold">Create</span>
      </div>
    </label>
    <section
      class="fixed top-10 right-4 hidden w-[200px] rounded-xl bg-[#242424] peer-checked:block"
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
  </div>
</template>

<style lang="scss" scoped></style>
