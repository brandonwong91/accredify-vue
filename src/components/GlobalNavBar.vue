<script setup lang="ts">
import IconHome from './icons/IconHome.vue'
import IconNote from './icons/IconNote.vue'
import IconLightBulb from './icons/IconLightBulb.vue'
import IconShield from './icons/IconShield.vue'
import IconCog from './icons/IconCog.vue'
</script>
<template>
  <nav class="w- flex flex-col h-[100vh]">
    <div class="h-5 w-5 p-5 mx-[10px] my-4 rounded-full bg-white self-center" />
    <div class="grid place-content-center">
      <div class="p-4 aspect-square hover:bg-[#353D4E] cursor-pointer">
        <IconHome />
      </div>
      <div class="p-4 aspect-square hover:bg-[#353D4E] cursor-pointer">
        <IconNote />
      </div>
      <div class="p-4 aspect-square hover:bg-[#353D4E] cursor-pointer">
        <IconLightBulb />
      </div>
      <div class="p-4 aspect-square hover:bg-[#353D4E] cursor-pointer">
        <IconShield />
      </div>
      <div class="p-4 aspect-square hover:bg-[#353D4E] cursor-pointer">
        <IconCog />
      </div>
    </div>
  </nav>
</template>
