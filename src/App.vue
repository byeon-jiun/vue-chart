<template>
  <div>
    <h1>Chart.js</h1>
    <bar-chart v-bind:barData="barChartDataSet"> </bar-chart>
    <line-chart v-bind:lineData="lineChartDataSet"></line-chart>
  </div>
</template>

<script>

import BarChart from "@/components/BarChart";
import LineChart from "@/components/LineChart";

export default {
  name: 'App',
  components: {LineChart, BarChart},
  data() {
    return {
      barChartDataSet: [{
          label: '# of Votes',
          data: [12, 19, 3, 5, 2, 3],
          backgroundColor: [
            'rgba(255, 99, 132, 0.2)',
            'rgba(54, 162, 235, 0.2)',
            'rgba(255, 206, 86, 0.2)',
            'rgba(75, 192, 192, 0.2)',
            'rgba(153, 102, 255, 0.2)',
            'rgba(255, 159, 64, 0.2)'
          ],
          borderColor: [
            'rgba(255, 99, 132, 1)',
            'rgba(54, 162, 235, 1)',
            'rgba(255, 206, 86, 1)',
            'rgba(75, 192, 192, 1)',
            'rgba(153, 102, 255, 1)',
            'rgba(255, 159, 64, 1)'
          ],
          borderWidth: 1
      }],
      lineChartDataSet: [{
          label: '# of Votes',
          data: [0, 10, 5, 2, 20, 30, 45],
          backgroundColor: [
            'rgb(255, 99, 132)'
          ],
          borderColor: [
            'rgb(255, 99, 132)'
          ]
      }]
    }
  }

}
</script>

<style>

</style>
