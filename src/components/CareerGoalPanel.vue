<script setup lang="ts">
import DoughnutChart from './DoughnutChart.vue'
</script>

<template>
  <div class="w-[260px] flex flex-col gap-y-4">
    <div class="font-bold text-xl leading-8">Career Goals</div>
    <div class="border rounded-md h-[433px] place-content-center grid gap-y-6 text-center">
      <div class="font-bold text-sm leading-6">Your Progress</div>
      <div class="h-[180px] w-[180px] aspect-auto flex flex-col place-content-center">
        <DoughnutChart class="absolute" />
        <div class="text-[#2B22B5] font-bold text-3xl">35%</div>
      </div>
      <div>
        <div class="text-sm leading-6">I want to be a</div>
        <div class="font-bold text-xl">Tax Manager</div>
      </div>
      <a class="text-[#493DF5] font-bold text-sm" href="#">View Insights</a>
    </div>
  </div>
</template>
