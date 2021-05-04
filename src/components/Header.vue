<template>
<header>
  <md-toolbar class="md-transparent" md-elevation="0">
    <md-icon>chevron_left</md-icon>
    <h3 class="md-title">Heather Tran</h3>
    <h3 class="md-title bold">/</h3>
    <md-icon>chevron_right</md-icon>
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
    color: white !important;
    text-shadow: 2px 2px 3px rgb(156, 156, 156);
    user-select: none;
    font: 1.5vw "Signika", sans-serif;
    margin-left: 10px !important;
}
@media (max-width: 1024px) {
    .md-title {
        font-size: 20px;
    }
}
.bold {
    font-weight: bolder;
}
i {
    margin: 0;
    color: white !important;
    text-shadow: 2px 2px 3px rgb(156, 156, 156);
    font-size: 30px !important;
}
</style>
