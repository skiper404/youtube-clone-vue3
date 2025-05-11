<script setup>
import CategoryItem from "./CategoryItem.vue";

const props = defineProps({ categories: Array, isActive: String });
const emit = defineEmits({ setActive: null });
</script>

<template>
  <ul class="flex items-center gap-2 overflow-auto px-2 py-1 whitespace-nowrap">
    <li v-for="category in categories" :key="category">
      <CategoryItem
        :category="category"
        :is-active="isActive"
        @click="emit('setActive', category)"
      />
    </li>
  </ul>
</template>
