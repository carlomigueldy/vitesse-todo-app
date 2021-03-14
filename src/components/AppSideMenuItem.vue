<script setup lang="ts">
import { defineProps } from "@vue/runtime-core";
// import { useRoute } from "vue-router";

// const route = useRoute()

const { label, icon } = defineProps({
  icon: {
    type: String,
    required: true,
  },
  label: {
    type: String,
    required: true,
  }
})
</script>

<template>
  <div class="hover:bg-green-100 hover:text-green-700 cursor-pointer bg-green-50 m-3 rounded-md p-3 text-green-600 font-bold">
    <!-- {{icon}} -->
    <component tag="mdi:home" is="mdi:home"></component>
    <app-tag :is="icon"></app-tag>
    <span>{{ label }}</span>
  </div>
</template>