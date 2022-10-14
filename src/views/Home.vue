<template>
  <div>
    <div class="row flex-wrap">
      <div class="col-sm d-flex justify-content-center">
        <radial-bar />
      </div>
      <div class="col-sm d-flex justify-content-center">
        <column />
      </div>
    </div>
  </div>
</template>

<script>
import RadialBar from "../components/RadialBar";
import Column from "../components/Column";

export default {
  name: "home",
  components: {
    "radial-bar": RadialBar,
    "column": Column
  },
};
</script>
<style>
.jumbotron {
  padding: 1rem 0rem;
}
</style>
