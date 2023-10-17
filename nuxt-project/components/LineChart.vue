<template>
  <Line id="my-chart-id" :options="chartOptions" :data="chartData" />
</template>

<script>
import { Line } from "vue-chartjs";
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  LineElement,
  CategoryScale,
  LinearScale,
  PointElement,
} from "chart.js";

ChartJS.register(Title, Tooltip, Legend, LineElement, CategoryScale, LinearScale, PointElement);

export default {
  name: "LineChart",
  components: { Line },
  data() {
    return {
      chartData: {
        labels: ["January", "February", "March", "April", "May"],
        datasets: [{ label: "data-set-1", data: [40, 20, 35, 18, 77] }],
        borderColor: "#36A2EB",
        backgroundColor: "#9BD0F5",
      },
    };
  },
};
</script>
