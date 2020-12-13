<script lang="ts">
// How it will work

// a numeric value with the color will be passed onto the chart
// if left ctrl is clicked delete that point,

import Vue from "vue";
import Component, { mixins } from "vue-class-component";
import { Line } from "vue-chartjs";

const LineChartProps = Vue.extend({
  props: {
    chartData: Object,
    options: Object,
  },
});

@Component
export default class LineChart extends mixins(Line, LineChartProps) {
  mounted() {
    this.renderChart(this.chartData, this.options);
  }
}
// Use these two functions first

// O(2n)
// function goingUpAndGoingDown(n: number): void {
//   console.log("Going up");
//   for (let i = 0; i < n; i++) {
//     console.log(i);
//   }
//   console.log("Going down");
//   for (let j = n - 1; j >= 0; j--) {
//     console.log(j);
//   }
// }

</script>