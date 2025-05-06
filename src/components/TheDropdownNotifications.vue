<script setup>
import {
  Bars3Icon,
  XMarkIcon,
  MagnifyingGlassIcon,
  PlusIcon,
  BellIcon,
} from "@heroicons/vue/24/outline";
import { MicrophoneIcon, EllipsisVerticalIcon } from "@heroicons/vue/24/solid";
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
import UserUpload from "./icons/userlogos/UserUpload.vue";
import UserCrearePost from "./icons/userlogos/UserCrearePost.vue";
import UserLive from "./icons/userlogos/UserLive.vue";

const randomSeed = () => Math.floor(Math.random() * Date.now());
</script>

<template>
  <div class="flex">
    <input type="checkbox" id="notifications" class="peer hidden" />
    <label for="notifications">
      <div class="rounded-full p-1 hover:bg-neutral-600">
        <BellIcon class="size-7" />
      </div>
    </label>
    <section
      class="fixed top-12 right-18 hidden h-[500px] w-[500px] rounded-2xl bg-[#242424] text-sm peer-checked:block"
    >
      <div class="flex items-center justify-between p-4">
        Notifications
        <UserSettings class="h-8 rounded-full p-1 hover:bg-[#555555]" />
      </div>
      <hr class="my-1 py-1 text-[#555555]" />
      <div>
        <ul class="flex flex-col">
          <li class="p-4 hover:bg-[#555555]">
            <a
              href="#"
              class="flex items-center justify-between gap-4 outline-none"
            >
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-12 w-12 rounded-full"
              />
              <div class="w-70 text-left text-sm">
                <p class="">Arthas is live: Последний из вас</p>
                <p class="font-light">1 days ago</p>
              </div>
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-9 w-16"
              />
              <button>
                <EllipsisVerticalIcon class="h-6" />
              </button>
            </a>
          </li>
          <li class="p-4 hover:bg-[#555555]">
            <a
              href="#"
              class="flex items-center justify-between gap-4 outline-none"
            >
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-12 w-12 rounded-full"
              />
              <div class="w-70 text-left text-sm">
                <p class="">
                  Bouleward Depo uploaded: Bouleward Depo - ДЫРБУЛЩИЩ
                </p>
                <p class="font-light">3 days ago</p>
              </div>
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-9 w-16"
              />
              <button>
                <EllipsisVerticalIcon class="h-6" />
              </button>
            </a>
          </li>
          <li class="p-4 hover:bg-[#555555]">
            <a
              href="#"
              class="flex items-center justify-between gap-4 outline-none"
            >
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-12 w-12 rounded-full"
              />
              <div class="w-70 text-left text-sm">
                <p class="">Янчик uploaded: Пересадка</p>
                <p class="font-light">6 days ago</p>
              </div>
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-9 w-16"
              />
              <button>
                <EllipsisVerticalIcon class="h-6" />
              </button>
            </a>
          </li>
          <li class="p-4 hover:bg-[#555555]">
            <a
              href="#"
              class="flex items-center justify-between gap-4 outline-none"
            >
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-12 w-12 rounded-full"
              />
              <div class="w-70 text-left text-sm">
                <p class="">Paul_Matteo uploaded: Тот самый друг</p>
                <p class="font-light">8 days ago</p>
              </div>
              <img
                :src="`https://picsum.photos/seed/${randomSeed()}/560/315`"
                alt="video_preview"
                class="h-9 w-16"
              />
              <button>
                <EllipsisVerticalIcon class="h-6" />
              </button>
            </a>
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped></style>
