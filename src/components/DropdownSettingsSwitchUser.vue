<script setup>
import BaseIcon from "./BaseIcon.vue";
import DropdownSettingsHeader from "./DropdownSettingsHeader.vue";

const emit = defineEmits({ selectMenu: null });
</script>

<template>
  <section
    class="fixed top-14 right-4 w-[300px] overflow-auto rounded-2xl bg-[#242424] peer-checked:block"
  >
    <DropdownSettingsHeader
      label="Accounts"
      description="Setting applies to this browser"
      @back="emit('select-menu', 'main')"
    />
    <div class="m-2 flex">
      <div class="m-2">
        <img
          :src="`https://picsum.photos/seed/${label}/560/315`"
          alt="video_preview"
          class="h-12 w-12 rounded-full border-2 border-blue-400"
        />
      </div>
      <div class="flex flex-col items-start">
        <span class="text-sm">John Doe</span>
        <span class="text-xs text-[#aaaaaa]">example@mail.com</span>
        <span class="text-xs text-[#aaaaaa]">No subscribrs</span>
      </div>
    </div>
    <div class="border-b border-[#555555] p-4 text-start text-sm">
      View all channel
    </div>
    <div class="flex items-center gap-2 p-2 hover:bg-[#555555]">
      <BaseIcon name="add-account" class="h-8" /><span>Add account</span>
    </div>
    <div class="flex items-center gap-2 p-2 hover:bg-[#555555]">
      <BaseIcon name="user-signout" class="h-8" />
      <span>Sign out</span>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
