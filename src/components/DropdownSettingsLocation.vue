<script setup>
import DropdownSettingListItem from "./DropdownSettingListItem.vue";
import DropdownSettingsHeader from "./DropdownSettingsHeader.vue";
const props = defineProps({ dropdownOptions: Object });
const countries = [
  "Argentina",
  "Brazil",
  "Canada",
  "France",
  "Germany",
  "Italy",
  "Japan",
  "Russia",
  "Ukraine",
  "USA",
];
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
      <li v-for="(countryName, countryId) in countries" :key="countryId">
        <DropdownSettingListItem
          :label="countryName"
          :active="countryId === dropdownOptions.location.id"
          @click="
            emit('setOption', {
              name: 'location',
              value: { id: countryId, label: countryName },
            })
          "
        />
      </li>
    </ul>
  </section>
</template>
<style lang="scss" scoped></style>
