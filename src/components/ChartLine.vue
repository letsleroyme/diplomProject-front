<div class="col l12">
  <div class="table-chart">
    <canvas id="canvas"></canvas>
  </div>
</div>

<script>
  import {Line} from 'vue-chartjs';
  export default {
    name: "ChartLine",
    data: () =>({
      chartData: ''
    }),
    extends: Line,
    mounted() {
      this.chartData = this.$store.state.table.chartData
      this.renderChart({
        labels: this.chartData.labels[1],
        datasets: [{
          label: this.chartData.header[1],
          data: this.chartData.data[1],
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
        }]
      })
    }
  }
</script>

<style scoped lang="scss">

</style>