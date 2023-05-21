<script setup lang="ts">
import DocumentTable from './DocumentTable.vue'
</script>
<template>
  <div class="w-full flex flex-col gap-y-4">
    <div class="flex justify-between">
      <div class="font-bold text-xl leading-8">Recent Documents</div>
      <a class="text-[#493DF5] font-bold text-sm" href="#">View All Documents</a>
    </div>
    <DocumentTable />
  </div>
</template>
