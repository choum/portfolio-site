<template>
  <md-card>
    <md-card-header class="md-display-2">
      <p>{{ title }}</p>
      <md-icon>{{ icon }}</md-icon>
    </md-card-header>
  </md-card>
</template>
<script>
import Vue from "vue";
import VueMaterial from "vue-material";
import "vue-material/dist/vue-material.min.css";
import "vue-material/dist/theme/default.css";

Vue.use(VueMaterial);
export default {
  name: "TitleCard",
  props: ["title", "icon"]
};
</script>

<style scoped lang="scss">
@import "../scss/_variable.scss";
p {
  margin: 0px;
  text-shadow: 3px 2px #9c9c9c;
}
.md-card {
  margin-top: 2em;
  width: 50%;
  background-color: $melon !important;
  width: calc(50% - 20px);
  user-select: none;
}
.md-display-2 {
  color: white !important;
  text-align: left;
  margin-left: 20px;
  font-size: 30pt;
  font-family: "Lato";
  font-weight: 700;
  margin-bottom: 0px;
}

.md-card-header {
  flex-direction: row;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.md-card {
  border-bottom: 7px white solid;
}
i {
  color: #fff !important;
  margin: 0;
  margin-top: 5px;
  margin-right: 20px;
  font-size: 30px !important;
}
</style>
