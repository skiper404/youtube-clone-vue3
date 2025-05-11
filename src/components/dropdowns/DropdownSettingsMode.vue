<script setup>
import DropdownSettingListItem from "./DropdownSettingListItem.vue";
import DropdownSettingsHeader from "./DropdownSettingsHeader.vue";
const props = defineProps({ dropdownOptions: Object });
const modeItems = ["On", "Off"];

const emit = defineEmits({ selectMenu: null });
</script>

<template>
  <section
    class="fixed top-14 right-4 w-[300px] overflow-auto rounded-2xl bg-[#242424] peer-checked:block"
  >
    <DropdownSettingsHeader
      label="Restricted Mode"
      description="Setting applies to this browser"
      @back="emit('select-menu', 'main')"
    />
    <ul class="text-sm">
      <li v-for="(mode, modeId) in modeItems" :key="modeId">
        <DropdownSettingListItem
          :label="mode"
          :active="modeId === dropdownOptions.mode.id"
          @click="
            emit('setOption', {
              name: 'mode',
              value: { id: modeId, label: mode },
            })
          "
        />
      </li>
    </ul>
  </section>
</template>
