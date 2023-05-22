<script setup lang="ts">
import IconBell from './icons/IconBell.vue'
import UserMenu from './UserMenu.vue'
</script>
<template>
  <div class="flex border-b-[#D0D2D6] h-16 border-b-[1px] place-content-end min-w-max">
    <div class="mr-12 flex gap-x-10 place-items-center">
      <IconBell />
      <UserMenu />
    </div>
  </div>
</template>
