<script setup lang="ts">
import CareerGoalPanel from '../components/CareerGoalPanel.vue'
import RecentDocumentsPanel from '../components/RecentDocumentsPanel.vue'
</script>

<template>
  <main class="px-36 pt-12 grid">
    <div class="grid gap-y-2">
      <h2 class="text-2xl leading-[44px] font-bold">Hi, Gerald Goh 👋</h2>
      <p class="text-[#5B6270]">
        Manage your documents issued by SMU Academy or track your career goal.
      </p>
      <div class="flex mt-14 gap-x-8">
        <CareerGoalPanel />
        <RecentDocumentsPanel />
      </div>
    </div>
  </main>
</template>
