<template>
    <div>
      <canvas ref="pieChartCanvas"></canvas>
    </div>
  </template>
  
  <script>
  import { Pie, mixins } from 'vue-chartjs';
  const { reactiveProp } = mixins;
  
  export default {
    extends: Pie,
    mixins: [reactiveProp],
    props: ['chartData', 'options'],
    mounted() {
      this.renderPieChart();
    },
    watch: {
      chartData() {
        this.renderPieChart();
      },
    },
    methods: {
      renderPieChart() {
        this.renderChart(this.chartData, this.options);
      },
    },
  };
  </script>
  
  <style scoped>
  
  </style>
  