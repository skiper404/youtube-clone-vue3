<script setup>
import UserGoogleLogo from "./icons/userlogos/UserGoogleLogo.vue";
import UserSwitchLogo from "./icons/userlogos/UserSwitchLogo.vue";
import UserSignOutLogo from "./icons/userlogos/UserSignOutLogo.vue";
import UserYouTubeStudio from "./icons/userlogos/UserYouTubeStudio.vue";
import UserPremium from "./icons/userlogos/UserPremium.vue";
import UserPurchase from "./icons/userlogos/UserPurchase.vue";
import UserData from "./icons/userlogos/UserData.vue";
import UserAppearence from "./icons/userlogos/UserAppearence.vue";
import UserLanguage from "./icons/userlogos/UserLanguage.vue";
import UserMode from "./icons/userlogos/UserMode.vue";
import UserLocation from "./icons/userlogos/UserLocation.vue";
import UserKeyboard from "./icons/userlogos/UserKeyboard.vue";
import UserSettings from "./icons/userlogos/UserSettings.vue";
import UserHelp from "./icons/userlogos/UserHelp.vue";
import UserFeedback from "./icons/userlogos/UserFeedback.vue";
import DropdownSettingListItem from "./DropdownSettingListItem.vue";
import { onUnmounted, ref, onMounted } from "vue";

const settingItems = [
  { label: "Google Account", icon: UserGoogleLogo },
  { label: "Switch Account", icon: UserSwitchLogo, submenu: true },
  { label: "Sign out", icon: UserSignOutLogo },
  { label: "YouTube studio", icon: UserYouTubeStudio },
  { label: "Your Premium Benefits", icon: UserPremium },
  { label: "Purchases and memberships", icon: UserPurchase },
  { label: "Your data in YouTube", icon: UserData },
  { label: "Appearence: Device theme", icon: UserAppearence, submenu: true },
  { label: "Restricted Mode: Off", icon: UserMode, submenu: true },
  { label: "Language: English", icon: UserLanguage, submenu: true },
  { label: "Location: Ukraine", icon: UserLocation, submenu: true },
  { label: "Keyboard shortcuts", icon: UserKeyboard },
  { label: "Settings", icon: UserSettings },
  { label: "Help", icon: UserHelp },
  { label: "Send feedback", icon: UserFeedback },
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
</script>

<template>
  <div class="relative" ref="wrapper">
    <img
      :src="`https://picsum.photos/200/200`"
      alt="video_preview"
      class="mr-2 h-10 w-10 rounded-full"
      @click="isOpen = true"
    />
  </div>
  <section
    v-if="isOpen"
    class="fixed top-12 right-4 w-[300px] overflow-auto rounded-2xl bg-[#242424] peer-checked:block"
  >
    <div class="flex">
      <img
        :src="`https://picsum.photos/560/315`"
        alt="video_preview"
        class="m-2 h-10 w-10 rounded-full px-2"
      />
      <div class="flex flex-col items-start py-2">
        <span>John Doe</span>
        <span>@Joundoe12</span>
        <a href="#" class="cursor-pointer py-1 text-blue-400 outline-none"
          >View your channel</a
        >
      </div>
    </div>
    <hr class="my-1 py-1 text-[#555555]" />
    <ul class="text-sm">
      <li v-for="item in settingItems" :key="item.label">
        <DropdownSettingListItem :item="item" />
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped></style>
