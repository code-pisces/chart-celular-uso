<template>
  <section class="cell-viewer">
    <div class="chart-container">
      <BarChart :chartData="data" />
    </div>
  </section>
</template>

<script lang="ts" setup>
import { BarChart } from 'vue-chart-3';
import { Chart, registerables } from "chart.js";

import { datasets } from "../database/smartphone-usage.json"

Chart.register(...registerables);
Chart.defaults.color = "#fff"
Chart.defaults.borderColor = 'rgba(255, 255, 255, 0.2)'

const labels = ["Domingo", 'Segunda', "Terça", "Quarta", "Quinta", "Sexta", "Sábado"];

const data = {
  labels,
  datasets
};
</script>

<style scoped>
section.cell-viewer {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 1000px;
  height: 520px;

}

@media (min-width: 1000px) {
  section.cell-viewer {
    background-image: url(../assets/iphone.png);
    background-position: center;
    background-repeat: no-repeat;
    background-size: 100%;
  }
}

.chart-container {
  width: 100%;
  height: 400px;
  max-width: 700px;
}
</style>