<template>
  <div class="mt-5 mb-5">
    <apexchart
      width="380"
      type="donut"
      :options="options"
      :series="series"
    ></apexchart>
  </div>
</template>
<script>
import VueApexCharts from "vue-apexcharts";
export default {
  components: {
    apexchart: VueApexCharts
  },
  data() {
    return {
      options: {},
      series: [44, 55, 41, 17, 15]
    };
  }
};
</script>
