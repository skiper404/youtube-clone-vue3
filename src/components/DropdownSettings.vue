<script setup>
import { ref, onMounted, onUnmounted, watch, computed, reactive } from "vue";
import DropdownSettingsMain from "./DropdownSettingsMain.vue";
import DropdownSettingsLanguage from "./DropdownSettingsLanguage.vue";
import DropdownSettingsAppearance from "./DropdownSettingsAppearance.vue";
import DropdownSettingsMode from "./DropdownSettingsMode.vue";
import DropdownSettingsLocation from "./DropdownSettingsLocation.vue";
import DropdownSettingsSwitchUser from "./DropdownSettingsSwitchUser.vue";

const isOpenMain = ref(false);
const selectedMenu = ref("main");

const dropdownOptions = reactive({
  language: { id: 0, label: "Russian" },
  location: { id: 0, label: "Ukrain" },
  theme: { id: 0, label: "Device theme" },
  mode: { id: 0, label: "Off" },
});

const setOption = (option) => {
  dropdownOptions[option.name] = option.value;
};

const menu = computed(() => {
  const dropdowns = {
    main: DropdownSettingsMain,
    appearance: DropdownSettingsAppearance,
    language: DropdownSettingsLanguage,
    mode: DropdownSettingsMode,
    location: DropdownSettingsLocation,
    switch: DropdownSettingsSwitchUser,
  };

  return dropdowns[selectedMenu.value];
});

const trigger = ref(null);
const activeDropdownRef = ref(null);

const showSelectedMenu = (menu) => {
  selectedMenu.value = menu;
  isOpenMain.value = true;
};

const triggerContainer = ref(null);

const handleClickOutside = (event) => {
  if (
    triggerContainer.value &&
    !triggerContainer.value.contains(event.target)
  ) {
    isOpenMain.value = false;
    selectedMenu.value = "";
  }
};

const handleKeydown = (event) => {
  if (event.key === "Escape") {
    isOpenMain.value = false;
    selectedMenu.value = "";
  }
};

onMounted(() => {
  window.addEventListener("click", handleClickOutside);
});

onUnmounted(() => {
  window.removeEventListener("click", handleClickOutside);
  window.removeEventListener("keydown", handleKeydown);
});

watch(isOpenMain, (newVal) => {
  if (newVal) {
    window.addEventListener("keydown", handleKeydown);
  } else {
    window.removeEventListener("keydown", handleKeydown);
  }
});
</script>

<template>
  <div ref="triggerContainer">
    <div class="relative" ref="trigger" @click.stop="showSelectedMenu('main')">
      <img
        :src="`https://picsum.photos/200/200`"
        alt="video_preview"
        class="mr-2 h-10 w-10 rounded-full"
      />
    </div>

    <transition
      enter-active-class="transition duration-200 ease-linear"
      enter-from-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="transition duration-200 ease-linear"
      leave-from-class="opacity-100"
      leave-to-class="opacity-0"
    >
      <component
        v-if="isOpenMain"
        :is="menu"
        @set-option="setOption"
        @select-menu="showSelectedMenu"
        ref="activeDropdownRef"
        :dropdown-options="dropdownOptions"
      ></component>
    </transition>
  </div>
</template>
