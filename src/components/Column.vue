<template>
  <div :style="{ width: 1200}" class="d-flex justify-content-center">
    <vue-apexcharts
      height="350"
      width="800"
      :options="chartOptions"
      :series="series"
    />
  </div>
</template>

<script>
import VueApexCharts from "vue-apexcharts";

export default {
  name: "RadialBar",
  components: {
    "vue-apexcharts": VueApexCharts,
  },
  data() {
    return {
      series: [
        {
          name: "NEW",
          data: [8, 15, 5, 12, 13, 14, 15, 5, 12],
        },
        {
          name: "RETURNING",
          data: [13, 12, 15, 8, 13, 12, 17, 15, 8],
        },
      ],
      chartOptions: {
        chart: {
          type: "bar",
          height: 350,
          stacked: true,
          toolbar: {
            show: false,
          },
          zoom: {
            enabled: false,
          },
        },
        colors: ["#6FC691", "#FCDE73"],
        responsive: [
          {
            breakpoint: 480,
            options: {
              legend: {
                position: "bottom",
                offsetX: -10,
                offsetY: 0,
              },
            },
          },
        ],
        dataLabels: {
          enabled: false,
        },
        plotOptions: {
          bar: {
            horizontal: false,
            borderRadius: 10,
            columnWidth: "30%",
            dataLabels: {
              enabled: false
            },
          },
        },
        xaxis: {
          categories: [
            ['Jan', '2022'],
            ['Feb', '2022'],
            ['Mar', '2022'],
            ['Apr', '2022'],
            ['May', '2022'],
            ['Jun', '2022'],
            ['Jul', '2022'],
            ['Aug', '2022'],
            ['Sep', '2022']
          ],
          labels: {
            style: {
              fontWeight: "bold",
            }
          },
        },
        yaxis: {
          opposite: true,
          maxWidth: "auto",
          tickAmount: 2,
          max: 32,
          labels: {
            style: {
              fontSize: "15px",
              fontWeight: "bold",
            },
          },
        },
        legend: {
          show: false,
        },
        fill: {
          opacity: 1,
        },
      },
    };
  },
};
</script>

<style scoped>
</style>>