<script setup lang="ts">
import { useRoute, useRouter } from "vue-router";

const router = useRouter()
const route = useRoute()
</script>

<template>
  <aside class="relative overflow-auto shadow-lg w-96 z-50 h-full">
    <div class="flex justify-center items-center w-full h-20 ">
      <div class="text-2xl">Vite Todo App</div>
    </div>

    <div class="my-10">
      <app-side-menu-item 
        :is-active="route.name === 'index'"
        label="Home"
        @click="router.push({ name: 'index' })"
      >
        <template #icon>
          <mdi:home class="mr-3" />
        </template>
      </app-side-menu-item>

      <app-side-menu-item 
        :is-active="route.name === 'settings'"
        label="Settings"
        @click="router.push({ name: 'settings' })"
      >
        <template #icon>
          <mdi:cog class="mr-3" />
        </template>
      </app-side-menu-item>
    </div>
 
    <div class="absolute bottom-0 left-0 right-0 p-5 flex justify-start items-center">
      <img src="https://pbs.twimg.com/profile_images/1366773484144054275/O2Lr3uzl_400x400.jpg"  
        class="object-cover rounded-full bg-gray-200 h-16 w-16" />
      <div class="w-4"></div>
      <div>
        <div class="text-lg">Carlo Miguel Dy</div>
        <div class="text-gray-400">carlomigueldy@gmail.com</div>
      </div>
    </div>
  </aside>
</template>
