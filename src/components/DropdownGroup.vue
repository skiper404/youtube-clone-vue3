<script setup>
import DropdownSettings from "./DropdownSettings.vue";
import DropdownNotifications from "./DropdownNotifications.vue";
import DropdownCreate from "./DropdownCreate.vue";
</script>

<template>
  <div class="hidden items-center justify-center gap-2 sm:flex">
    <DropdownCreate />
    <DropdownNotifications />
    <DropdownSettings />
  </div>
</template>

<style lang="scss" scoped></style>
