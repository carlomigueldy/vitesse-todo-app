<script setup lang="ts">
import { defineProps } from "@vue/runtime-core";
// import { useRoute } from "vue-router";

// const route = useRoute()

const { label } = defineProps({
  isActive: {
    type: Boolean,
  },
  label: {
    type: String,
    required: true,
  }
})
</script>

<template>
  <div :class="{
    'hover:bg-blue-100': true,
    'hover:text-blue-700': true,
    'bg-blue-50': isActive,
    'cursor-pointer': true,
    'm-3': true,
    'rounded-md': true,
    'p-3': true,
    'text-blue-600': true,
    'font-bold': true
  }">
    <slot name="icon"></slot>
    <span>{{ label }}</span>
  </div>
</template>