<template>
  <div>
    <LineChartGenerator :data="chartData" :options="chartOptions" />
  </div>
</template>

<script>
import { Line } from "vue-chartjs";
import { Chart as ChartJS, Title, Tooltip, Legend, LineElement, CategoryScale, LinearScale, PointElement } from "chart.js";

ChartJS.register(Title, Tooltip, Legend, LineElement, CategoryScale, LinearScale, PointElement);

export default {
  name: "LineChart",
  components: { LineChartGenerator: Line },
  data() {
    return {
      chartData: {
        labels: ["Jan", "Feb", "Mar", "Apr", "May"],
        datasets: [
          {
            label: "Users",
            data: [40, 60, 80, 100, 120],
            borderColor: "blue",
            fill: false
          }
        ]
      },
      chartOptions: { responsive: true, maintainAspectRatio: false }
    };
  }
};
</script>