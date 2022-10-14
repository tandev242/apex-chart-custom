<template>
  <vue-apexcharts
    height="350"
    width="400"
    :options="chartOptions"
    :series="series"
  />
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
      series: [30, 40],
      chartOptions: {
        chart: {
          type: "radialBar",
        },
        dataLabels: {
          enabled: false,
        },
        responsive: [
          {
            breakpoint: 300,
            options: {
              chart: {
                width: 200,
              },
              legend: {
                show: false,
              },
            },
          },
        ],
        colors: ["#6FC691", "#83CDD9"],
        legend: {
          position: "right",
          offsetY: 0,
          height: 230,
        },
        plotOptions: {
          radialBar: {
            hollow: {
              size: "20%",
              background: "transparent",
              image: undefined,
              imageWidth: 150,
              imageHeight: 150,
              imageOffsetX: 0,
              imageOffsetY: 0,
              imageClipped: true,
              position: "front",
              dropShadow: {
                enabled: false,
                top: 0,
                left: 0,
                blur: 3,
                opacity: 0.5,
              },
            },
            track: {
              margin: 23,
              background: ["#4678CC", "#8657AC"],
            },
            dataLabels: {
              name: {
                show: false,
              },
              value: {
                fontSize: "30px",
                show: true,
              },
            },
          },
        },
      },
    };
  },
};
</script>
