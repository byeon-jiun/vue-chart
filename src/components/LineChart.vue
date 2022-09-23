<template>
  <canvas id="lineChart" ref="line"></canvas>
</template>

<script>
export default {
  name: "LineChart",
  props: {
    lineData: []
  },
  mounted() {
    const ctx = this.$refs.line.getContext('2d')
    const lineChart = new this.$_Chart(ctx, {
          type: 'line',
          data: {
            labels: [ 'January',
              'February',
              'March',
              'April',
              'May',
              'June'],
            datasets: this.lineData
          },
          options: {
          }
        }
    );

    console.log(lineChart)
  }
}
</script>

<style scoped>

</style>