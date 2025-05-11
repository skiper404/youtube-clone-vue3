<script setup>
import DropdownSettingListItem from "./DropdownSettingListItem.vue";
import DropdownSettingsHeader from "./DropdownSettingsHeader.vue";
const props = defineProps({ dropdownOptions: Object });

const themeItems = ["Use device theme", "Dark theme", "Light theme"];

const emit = defineEmits({ setOption: null });
</script>

<template>
  <section
    class="fixed top-14 right-4 w-[300px] overflow-auto rounded-2xl bg-[#242424] peer-checked:block"
  >
    <DropdownSettingsHeader
      label="Appearence"
      description="Setting applies to this browser"
      @back="emit('select-menu', 'main')"
    />
    <ul class="text-sm">
      <li v-for="(themeName, themeId) in themeItems" :key="themeId">
        <DropdownSettingListItem
          :label="themeName"
          :active="themeId === dropdownOptions.theme.id"
          @click="
            emit('setOption', {
              name: 'theme',
              value: { id: themeId, label: themeName },
            })
          "
        />
      </li>
    </ul>
  </section>
</template>
