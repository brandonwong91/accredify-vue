<script>
import { useRoute } from 'vue-router'
import CareerGoalPanel from '../components/CareerGoalPanel.vue'
import RecentDocumentsPanel from '../components/RecentDocumentsPanel.vue'
import axios from 'axios'
export default {
  data() {
    console.log(this.$route, this.$router)
    return {
      info: null,
      isPersonal: false,
      name: '',
      documents: [],
      progress: 0,
      nextPromotion: ''
    }
  },
  mounted() {
    axios
      .get(`http://localhost:5174/users/${this.$route.query.user}`)
      .then((response) => (this.info = response))
      .then((info) => {
        const { current_organisation, name, documents } = info.data
        this.isPersonal = current_organisation.is_personal
        this.name = name
        this.documents = documents
        this.progress = current_organisation.career_goals.progress
        this.nextPromotion = current_organisation.career_goals.name
      })
  },
  components: {
    CareerGoalPanel,
    RecentDocumentsPanel
  }
}
</script>

<template>
  <main class="px-12 xl:px-36 pt-12 grid">
    <div class="grid gap-y-2">
      <h2 class="text-2xl leading-[44px] font-bold">
        Hi,
        <span v-if="name" class="text-2xl leading-[44px] font-bold">{{ name }}</span>
        <span v-else class="text-2xl leading-[44px] font-bold">Gerald Goh</span>
        👋
      </h2>
      <p class="text-[#5B6270]">
        Manage your documents issued by SMU Academy or track your career goal.
      </p>
      <div class="flex mt-14 gap-x-8">
        <div v-if="isPersonal || $route.query.chart">
          <CareerGoalPanel :progress="progress" :next-promotion="nextPromotion" />
        </div>
        <RecentDocumentsPanel />
      </div>
    </div>
  </main>
</template>
