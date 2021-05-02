<template>
  <header>
    <md-toolbar class="md-transparent" md-elevation="0">
      <h3 class="md-title">Heather Tran</h3>
    </md-toolbar>
  </header>
</template>

<script>
import Vue from "vue";
import VueMaterial from "vue-material";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";

Vue.use(VueMaterial);

export default {
  name: "Header"
};
</script>

<style scoped lang="scss">
@import "../scss/_variable.scss";
.md-title {
  color: $isabelline !important;
  font: 1.5vw "Signika", sans-serif;
}
</style>
