<script setup>
import DropdownSettingsHeader from "./DropdownSettingsHeader.vue";
import DropdownSwithUserMain from "./DropdownSwithUserMain.vue";

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
    <DropdownSwithUserMain :label="label" />
  </section>
</template>
