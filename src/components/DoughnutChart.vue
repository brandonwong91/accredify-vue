<template>
  <Doughnut :data="data" :options="options" />
</template>

<script>
import { Doughnut } from 'vue-chartjs'

import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'

ChartJS.register(ArcElement, Tooltip, Legend)

export default {
  name: 'DoughnutChart',
  components: { Doughnut },
  data() {
    return {
      data: {
        datasets: [
          {
            backgroundColor: ['#493DF5', '#E8E9EB'],
            data: [35, 65]
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        cutout: '80%',
        borderRadius: 20
      }
    }
  }
}
</script>
