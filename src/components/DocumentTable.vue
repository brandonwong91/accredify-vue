<script setup lang="ts">
import IconDocument from './icons/IconDocument.vue'
import IconKebab from './icons/IconKebab.vue'
</script>
<template>
  <div class="border rounded-md h-[433px] px-6 py-8">
    <div class="flex pb-5 border-b justify-between">
      <div class="pl-4 font-bold text-sm leading-6 text-start">Document Name</div>
      <div class="col-span-1 font-bold text-sm leading-6 pr-24">Received On</div>
    </div>
    <div class="flex-col flex divide-y border-b">
      <div class="flex h-16 place-items-center justify-between">
        <div class="flex min-w-[580px] gap-5 align-middle">
          <IconDocument />
          <div class="font-bold text-sm leading-6 truncate max-w-[390px]">
            Degree in Information Systems
          </div>
        </div>
        <div class="flex place-items-center gap-x-10 pr-4">
          <div>29 June 2021</div>
          <IconKebab class="self-center" />
        </div>
      </div>
      <div class="flex h-16 place-items-center justify-between">
        <div class="flex min-w-[580px] gap-5 align-middle">
          <IconDocument />
          <div class="font-bold text-sm leading-6 truncate max-w-[390px]">
            Fintech: Foundations and Applications of Financial Technol
          </div>
        </div>
        <div class="flex place-items-center gap-x-10 pr-4">
          <div>29 June 2021</div>
          <IconKebab class="self-center" />
        </div>
      </div>
    </div>
  </div>
</template>
