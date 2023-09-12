<template>
  <Bar
    id="my-chart-id"
    :options="chartOptions"
    :data="chartData"
  />
</template>

<script>
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

export default {
  name: 'BarChart',
  components: { Bar },
  data() {
    return {
      chartData: {
        labels: [ 'Fazenda Mumba', 'Fazenda Jamba', 'Fazenda Girassol' ],
        datasets: [ { data: [7, 10, 12] } ]
      },
      chartOptions: {
        responsive: true
      }
    }
  }
}
</script>