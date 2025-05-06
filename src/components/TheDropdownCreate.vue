<script setup>
import { PlusIcon } from "@heroicons/vue/24/outline";

import UserUpload from "./icons/userlogos/UserUpload.vue";
import UserCrearePost from "./icons/userlogos/UserCrearePost.vue";
import UserLive from "./icons/userlogos/UserLive.vue";
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
        <li class="py-2 hover:bg-[#555555]">
          <a href="#" class="flex items-center gap-4 px-6 outline-none">
            <UserUpload class="h-6" /> Upload video
          </a>
        </li>
        <li class="py-2 hover:bg-[#555555]">
          <a href="#" class="flex items-center gap-4 px-6 outline-none"
            ><UserLive class="h-6" /> Go Live
          </a>
        </li>
        <li class="py-2 hover:bg-[#555555]">
          <a href="#" class="flex items-center gap-4 px-6 outline-none">
            <UserCrearePost class="h-6" />
            Create post
          </a>
        </li>
      </ul>
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
