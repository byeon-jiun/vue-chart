<template>
  <canvas id="barChart" width="400" height="400" ref="bar"></canvas>
</template>

<script>

export default {
  name: "BarChart",
  props: {
    barData: []
  },
  mounted() {
    const ctx = this.$refs.bar;
    const barChart = new this.$_Chart(ctx, {
      type: 'bar',
      data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: this.barData
      },
      options: {
        scales: {
          y: {
            beginAtZero: true
          }
        }
      }
    });
    console.log(barChart)
  }
}
</script>

<style scoped>

</style>