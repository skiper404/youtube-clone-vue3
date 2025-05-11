<script setup>
import DropdownSettingListItem from "./DropdownSettingListItem.vue";
import DropdownSettingsHeader from "./DropdownSettingsHeader.vue";

const props = defineProps({ dropdownOptions: Object });

const languages = ["Russian", "Ukrainian", "English"];

const emit = defineEmits({ setOption: null });
</script>

<template>
  <section
    class="fixed top-14 right-4 w-[300px] overflow-auto rounded-2xl bg-[#242424] peer-checked:block"
  >
    <DropdownSettingsHeader
      label="Location"
      description="Setting applies to this browser"
      @back="emit('select-menu', 'main')"
    />
    <ul class="text-sm">
      <li v-for="(languageName, languageId) in languages" :key="languageId">
        <DropdownSettingListItem
          :label="languageName"
          :active="languageId === dropdownOptions.language.id"
          @click="
            emit('setOption', {
              name: 'language',
              value: { id: languageId, label: languageName },
            })
          "
        />
      </li>
    </ul>
  </section>
</template>
