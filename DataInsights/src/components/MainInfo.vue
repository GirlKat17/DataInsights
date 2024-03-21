<template>
    <div>
      <pie-chart :chartData="pieChartData" :options="pieChartOptions"></pie-chart>
    </div>
  </template>
  
  <script>
  import PieChart from './components/PieChart.vue';
  import pieChartData from '/pieChart.json'; 
  
  export default {
    components: {
      PieChart,
    },
    data() {
      return {
        pieChartData: pieChartData,
        pieChartOptions: {} 
      };
    },
  };
  </script>
  
  <style scoped>
  
  </style>
  