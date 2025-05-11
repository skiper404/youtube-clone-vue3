<script setup>
import DropdownSettings from "./DropdownSettings.vue";
import DropdownNotifications from "./DropdownNotifications.vue";
import DropdownCreate from "./DropdownCreate.vue";
import BaseTooltip from "../BaseTooltip.vue";
</script>

<template>
  <div class="hidden items-center justify-center gap-2 sm:flex">
    <BaseTooltip label="Create">
      <DropdownCreate />
    </BaseTooltip>
    <BaseTooltip label="Notifications">
      <DropdownNotifications />
    </BaseTooltip>
    <BaseTooltip label="User">
      <DropdownSettings />
    </BaseTooltip>
  </div>
</template>
