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
</script>

<template>
  <div>
    <input type="checkbox" id="usermenu" class="peer hidden" />
    <label for="usermenu">
      <img
        :src="`https://picsum.photos/560/315`"
        alt="video_preview"
        class="h-10 w-10 rounded-full"
      />
    </label>
    <section
      class="fixed top-12 right-4 z-50 hidden w-[300px] overflow-auto rounded-2xl bg-[#242424] peer-checked:block"
    >
      <div class="flex">
        <img
          :src="`https://picsum.photos/560/315`"
          alt="video_preview"
          class="m-2 h-10 w-10 rounded-full"
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
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserGoogleLogo class="h-6" />Google Account</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserSwitchLogo class="h-6" />Switch Account</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserSignOutLogo class="h-6" />Sign out</a
          >
        </li>
        <hr class="my-2 text-[#555555]" />
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserYouTubeStudio class="h-6" />YouTube studio</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserPremium class="h-6" />Your Premium Benefits</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserPurchase class="h-6" />Purchases and memberships</a
          >
        </li>
        <hr class="my-2 text-[#555555]" />
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserData class="h-6" />Your data in YouTube</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserAppearence class="h-6" />Appearence: Device theme</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserLanguage class="h-6" />Language: English</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserMode class="h-6" />Restricted Mode: Off</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserLocation class="h-6" />Location: Ukraine</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserKeyboard class="h-6" />Keyboard shortcuts</a
          >
        </li>
        <hr class="my-2 text-[#555555]" />
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserSettings class="h-6" />Settings</a
          >
        </li>
        <hr class="my-2 text-[#555555]" />
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserHelp class="h-6" />Help</a
          >
        </li>
        <li class="p-2 hover:bg-[#555555]">
          <a href="" class="flex items-center gap-4 outline-none"
            ><UserFeedback class="h-6" />Send feedback</a
          >
        </li>
      </ul>
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
