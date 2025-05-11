<script setup>
import { reactive } from "vue";
import DropdownSettingListItem from "./DropdownSettingListItem.vue";
import DropdownMainHeader from "./DropdownMainHeader.vue";
const props = defineProps({ dropdownOptions: Object });
const emit = defineEmits({ selectMenu: null, setOption: null });

const settingItems = reactive([
  { id: "google", label: "Google Account", icon: "user-google" },
  { id: "switch", label: "Switch Account", icon: "user-switch", submenu: true },
  { id: "sighout", label: "Sign out", icon: "user-signout" },
  { id: "studio", label: "YouTube studio", icon: "user-studio" },
  { id: "premium", label: "Your Premium Benefits", icon: "user-premium" },
  { id: "purchase", label: "Purchases and memberships", icon: "user-purchase" },
  { id: "data", label: "Your data in YouTube", icon: "user-data" },
  {
    id: "appearance",
    label: "Appearence: " + props.dropdownOptions.theme.label,
    icon: "user-apperiance",
    submenu: true,
  },
  {
    id: "language",
    label: "Language: " + props.dropdownOptions.language.label,
    icon: "user-language",
    submenu: true,
  },
  {
    id: "mode",
    label: "Restricted Mode: " + props.dropdownOptions.mode.label,
    icon: "user-mode",
    submenu: true,
  },
  {
    id: "location",
    label: "Location: " + props.dropdownOptions.location.label,
    icon: "user-location",
    submenu: true,
  },
  { id: "keyboard", label: "Keyboard shortcuts", icon: "user-keyboard" },
  { id: "settings", label: "Settings", icon: "user-settings" },
  { id: "help", label: "Help", icon: "user-help" },
  { id: "feedback", label: "Send feedback", icon: "user-feedback" },
]);
</script>

<template>
  <section
    class="fixed top-14 right-4 w-[300px] overflow-auto rounded-2xl bg-[#242424]"
  >
    <DropdownMainHeader />
    <hr class="my-1 py-1 text-[#555555]" />
    <ul class="text-sm">
      <li
        v-for="item in settingItems"
        :key="item.label"
        @click.stop="emit('select-menu', item.id)"
      >
        <DropdownSettingListItem
          :label="item.label"
          :icon="item.icon"
          :submenu="item.submenu"
        />
      </li>
    </ul>
  </section>
</template>
