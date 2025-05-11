<script setup>
import DropdownCreateListItem from "../dropdowns/DropdownCreateListItem.vue";
const props = defineProps({ menuItems: Array });
</script>

<template>
  <ul
    class="fixed top-12 right-4 my-2 w-50 rounded-xl bg-[#242424] py-2 text-sm"
  >
    <li
      class="py-2 hover:bg-[#555555]"
      v-for="item in menuItems"
      :key="item.label"
    >
      <DropdownCreateListItem :item="item" />
    </li>
  </ul>
</template>
