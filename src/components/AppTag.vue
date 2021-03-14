<script setup lang="ts">
import { defineProps } from "@vue/runtime-core";

const { is } = defineProps({
  is: {
    type: String,
    required: true,
  }
})
</script>

<template>
  <div :id="`replace-${is}`"></div>
</template>